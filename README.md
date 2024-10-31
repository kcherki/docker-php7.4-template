# Docker PHP 7.4 Development Environment

![PHP Version](https://img.shields.io/badge/PHP-7.4-blue?logo=php)
![Apache Version](https://img.shields.io/badge/Apache-2.4-orange?logo=apache)
![MySQL Version](https://img.shields.io/badge/MySQL-5.7-blue?logo=mysql)
![Docker](https://img.shields.io/badge/Docker-ready-blue?logo=docker)

This project provides a ready-to-use Docker development environment for PHP 7.4 with Apache and MySQL, ideal for PHP projects.

## Objective
The purpose of this template is to simplify the setup of a standard PHP development environment. With this Docker stack, you can quickly start projects, test, and deploy PHP applications with a complete configuration.

## Technical Stack
- **PHP**: version 7.4
- **Apache**: version 2
- **MySQL**: version 5.7
- **PHP Extensions**: PDO, GD, and others.

## Installation

1. **Clone this repository**:

    ```bash
    git clone https://github.com/your-username/docker-php7.4-template.git my-project
    ```

2. **Create the `www` folder for your code**:

    ```bash
    mkdir www
    ```

3. **Launch Docker services**:

    ```bash
    docker-compose up -d
    ```

## Configuration

### Web Access
- URL: [http://localhost](http://localhost)

### Database

```code
Host: localhost
Port: 3306
Database: my_database
Username: my_user
Password: my_password
```

### Usage

- Add your PHP files to the `www/` folder to make them accessible within your development environment.
- Any changes made to the files in the `www/` folder are immediately visible in the browser.
###Accessing Logs
To track errors and events for each service, use the following command:

```bash
docker-compose logs
```
This Docker template provides a solid base to develop and test your PHP applications, streamlining your workflow.

```bash
This structure includes GitHub-formatted command blocks, making it easy to follow for users who copy it into their own repositories.
```