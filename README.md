# Nextcloud quick start

Start Your Own Cloud in minutes

![Files page Screenshot](images/Screenshot4.png "Files page Screenshot")

##What is Nextcloud

Nextcloud is a self-hosted productivity platform that offers secure file sharing, collaboration, and cloud storage. It empowers users to retain control over their data while providing features comparable to popular cloud services. Nextcloud’s flexibility can be expanded with popular add-ons like Calendar for scheduling, Contacts for managing personal and shared contacts, Deck for project management, OnlyOffice/Collabora Online for real-time document editing, and Talk for secure video calls and chat. With its rich ecosystem, Nextcloud is ideal for both personal use and enterprise-level deployment.

## How It Works

- **Nextcloud and Cron** - The main functionality of Nextcloud.
- **PostgreSQL** - Database for administrative data storage.
- **Redis** - Caching backend.
- **Nginx-proxy** - Automated Nginx Reverse Proxy.
- **Omgwtfssl** - Self Signed SSL Certificate Generator.
- **Letsencrypt-companion** - Automated creation, renewal and use of SSL certificates.

You can use only one of Omgwtfssl (for selfsigned local HTTPS) or Letsencrypt-companion (for SSL/TLS Letsencrypt secured HTTPS, you need to have a configured domain)

## Bringing Code onto Your Host

1. Ensure you have Git or another tool to clone repositories. [Download Git here](https://git-scm.com/downloads).
2. Clone the `nextcloud` code to your host:
   - Prepare a directory for the code.
   - Open a terminal in this directory.
   - Run the clone command:
     ```bash
     git clone https://github.com/androg9n/nextcloud.git
     ```
   - Navigate into the directory with the cloned code:
     ```bash
     cd nextcloud
     ```
# Starting with Docker Compose

## Prerquisites

1. Docker Compose is installed on your host. [Installation instructions](https://docs.docker.com/compose/install/).

## Configuration (Optional)

Default configuration suppose the Selfsigned local use.

## Starting

1. Open a terminal in the `nextcloud` code directory.
2. Navigate to the `docker-compose` directory:
   ```bash
   cd docker-compose 
   ```
3. Start the services with the command: `docker compose up -d`.
   ```bash
   docker compose up -d
   ```
4. Open Nextcloud in your web browser using configured domain address (default [https://cloud.home](https://cloud.home)).
5. If you use selfsigned certificate it will be nessecary to accept the security risk at first time open the page.

![The First time opening warning for the Selfsigned HTTPS](images/Screenshot1.png "Security Warning")

## Stopping and removing

1. To stop the services, run from the `docker-compose` directory:
   ```bash
   docker compose down
   ```
2. To delete all collected service data, run from the same directory (be carefull!!! all data will be lost!!!):
   ```bash
   docker compose down -v
   ```

[🏠 Back to Main README](..)
