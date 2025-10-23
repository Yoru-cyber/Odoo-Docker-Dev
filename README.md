# Odoo Development Stack

A Docker Compose setup for running Odoo with PostgreSQL database, ideal for development and testing environments.

## 📋 Prerequisites

- Docker
- Docker Compose

## 🛠️ Quick Start

1. Clone or create the project directory:

```bash
git clone https://github.com/Yoru-cyber/Odoo-Docker-dev.git
```

2. Create your the addons directory for your custom Odoo modules:

```bash
mkdir addons
```

3. Create the .env file:

```bash
cp .env.example .env
```
4. Access Odoo:

Open your browser and go to: http://localhost:${ODOO_WEB_PORT}/web

## 📁 Project Structure

```sh
odoo17-dev/
├── docker-compose.yml
├── entrypoint.sh          # Custom entrypoint script
├── postgresql/           # PostgreSQL data directory
├── addons/               # Custom Odoo modules
└── etc/                  # Odoo configuration files
```

## Error with permissions

```bash
sudo chown -R $USER:$USER postgresql
sudo chown -R $USER:$USER addons
sudo chown -R $USER:$USER etc
```

## 🛠️ Version Management

Switching Odoo Versions
To switch to a different Odoo version, simply update the .env file:
```env
ODOO_VERSION=16.0
ODOO_WEB_PORT=10016
ODOO_CHAT_PORT=20016
```
Switching PostgreSQL Versions
Update the PostgreSQL version in the .env file:

```env
POSTGRES_VERSION=15
```

Example for Odoo 16

```env
ODOO_VERSION=16.0
ODOO_WEB_PORT=10016
ODOO_CHAT_PORT=20016
POSTGRES_VERSION=15
```
