# Docker PHP 7.4 Development Environment

Template Docker pour projets PHP 7.4 avec Apache et MySQL.

## Stack technique

- PHP 7.4
- Apache 2
- MySQL 5.7
- Extensions PHP : PDO, GD, etc.

## Installation

1. Clonez ce repository : 


git clone https://github.com/votre-username/docker-php7.4-template.git mon-projet

2. Créez le dossier www pour votre code :

mkdir www


docker-compose up -d


## Configuration

### Accès Web
- URL: http://localhost

### Base de données
- Host: localhost
- Port: 3306
- Database: ma_base
- Username: mon_user
- Password: mon_password

## Utilisation

- Placez vos fichiers PHP dans le dossier `www/`
- Les modifications sont immédiatement visibles
- Accès aux logs : `docker-compose logs`