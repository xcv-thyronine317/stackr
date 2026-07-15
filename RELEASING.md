# Releasing Stackr

Stackr auto-updates via Tauri's updater. Because this repo is **public**, its own
Release assets are reachable unauthenticated, so releases are published **here** —
no separate manifest repo and no cross-repo token. The app checks:

```
https://github.com/igrdkl/stackr/releases/latest/download/latest.json
```

and offers the update in **Settings → Updates**.

## One-time setup

The **public** signing key is committed in `src-tauri/tauri.conf.json`
(`plugins.updater.pubkey`). The **private** key was generated locally at:

```
%USERPROFILE%\.tauri\stackr-updater.key
```

It is **not** in the repo and must never be committed. Add these two secrets to the
repo (Settings → Secrets and variables → Actions):

| Secret | Value |
|--------|-------|
| `TAURI_SIGNING_PRIVATE_KEY` | entire contents of `%USERPROFILE%\.tauri\stackr-updater.key` |
| `TAURI_SIGNING_PRIVATE_KEY_PASSWORD` | the key's password (empty — it was generated without one) |

> The default `GITHUB_TOKEN` publishes the Release; no Personal Access Token is
> needed now that the repo is public.
>
> Keep a backup of the private key. If it's lost, existing installs can no longer
> verify updates and users must reinstall manually.

## Cutting a release

1. Bump the version in **three** files (keep them in sync):
   `package.json`, `src-tauri/Cargo.toml`, `src-tauri/tauri.conf.json`.
2. Commit, then tag and push:
   ```bash
   git tag v0.3.0
   git push origin v0.3.0
   ```
3. The **release** workflow builds + signs the installer and publishes it with a
   generated `latest.json` to this repo's Releases, named for the tag (no draft, so
   the updater endpoint resolves immediately).

Existing installs pick up the update on their next launch (or via
**Settings → Updates → Check for updates**).
