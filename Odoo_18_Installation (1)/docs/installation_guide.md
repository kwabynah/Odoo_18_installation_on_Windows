# Installation Guide

Detailed steps for installing Odoo 18 on Windows. Follow each step carefully for a seamless setup.
Odoo ERP Installation and Configuration on Windows

1. System Requirements

Before installing Odoo 18 on Windows, ensure your system meets the following requirements:

Windows 10 or later (64-bit recommended)

Minimum 8GB RAM (16GB recommended for optimal performance)

At least 20GB of free disk space

PostgreSQL 14+ Database (required for Odoo to function)

Python 3.10+

Node.js 16+ (for frontend assets)

Git (optional, but recommended for version control)

2. Download and Install Odoo

Visit the Odoo official website and download the latest Odoo 18 Windows installer.

Run the installer and follow these steps:

Select the components to install (Odoo and PostgreSQL required).

Choose an installation directory (default is usually fine).

Set an admin password for PostgreSQL.

Complete the installation process.

3. Configuring PostgreSQL Database

Odoo uses PostgreSQL as its database backend. If PostgreSQL is installed during Odoo setup:

Open pgAdmin (PostgreSQL's management tool).

Log in with the admin password you set during installation.

Create a new database named odoo18.

Create a new PostgreSQL user for Odoo with all privileges on the odoo18 database.

4. Running Odoo

Navigate to the Odoo installation folder.

Run the odoo-bin.exe file or start Odoo from the Windows Start Menu.

Alternatively, use the provided start_odoo.bat script:

@echo off
cd /d "C:\Program Files\Odoo 18\server"
python odoo-bin --config="C:\Program Files\Odoo 18\server\odoo.conf"

Open a web browser and go to http://localhost:8069.

Follow the on-screen setup to create a new Odoo database and admin account.

5. Basic Configuration

Setting Up Users: Go to Settings > Users and add new users as needed.

Installing Modules: Navigate to Apps, search for necessary modules (like CRM, Sales, Inventory), and install them.

Configuring Email: Set up an outgoing mail server in Settings > General Settings > Email to send notifications.

Configuring Odoo.conf: Place the sample odoo.conf file in C:\Program Files\Odoo 18\server\config\.

6. Troubleshooting

If Odoo does not start, check the logs in the Odoo installation folder (odoo.log).

If PostgreSQL fails, ensure it is running by checking services.msc and restarting the PostgreSQL service.

If frontend assets are not loading, install the necessary dependencies:

npm install -g less less-plugin-clean-css

If running Python scripts fails, ensure you have installed dependencies using:

pip install -r requirements.txt

7. Additional Resources

Odoo Documentation: https://www.odoo.com/documentation

Odoo Community Forum: https://www.odoo.com/forum
