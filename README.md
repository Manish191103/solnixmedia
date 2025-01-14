# Solnix Media Docker Setup

## Overview
This Docker Compose setup provides a complete development environment for Solnix Media, including:
- MariaDB database
- phpMyAdmin for database management
- WordPress CMS

## Requirements
- Docker
- Docker Compose

## Setup Instructions

1. Clone this repository
2. Create a `.env` file using the template below
3. Run `docker-compose up -d`

## .env File Template
```env
# Database Configuration
MYSQL_ROOT_PASSWORD=your_secure_password
MYSQL_DATABASE=solnix_db
MYSQL_USER=solnix_user
MYSQL_PASSWORD=your_secure_password

# WordPress Configuration
WORDPRESS_DB_HOST=database:3306
WORDPRESS_DB_USER=wp_user
WORDPRESS_DB_PASSWORD=your_secure_password
WORDPRESS_DB_NAME=wordpress_db
```

## Security Best Practices
- Use unique, strong passwords for each account
- Never commit .env files to version control
- Regularly update Docker images to latest versions
- Use separate database users for WordPress and admin access
- Consider implementing SSL/TLS for database connections

## Access URLs
- WordPress: http://localhost:8082
- phpMyAdmin: http://localhost:8081

## Maintenance
- To stop containers: `docker-compose down`
- To view logs: `docker-compose logs -f`
- To update containers: `docker-compose pull && docker-compose up -d`