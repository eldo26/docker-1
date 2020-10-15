# docker (nginx, php, mysql, phpmyadmin)

# Install Docker

- Windows: https://docs.docker.com/docker-for-windows/install/
- Linux: https://docs.docker.com/engine/install/ubuntu/
- Mac: https://docs.docker.com/docker-for-mac/install/

# Create a project folder

- git clone https://github.com/ronaldwilson/docker.git project-name

# Clone Laravel project

- cd project-name
- Clone Laravel project to src/ directory
  - git clone https://github.com/Renfos/Lavalite.git src

# Spin containers

- Run following command to spin all containers:
  - docker-compose up -d

# Update Laravel DB credentials

- cd src/ folder
- composer install
- npm install
- npm run dev
- cp .env.example .env

- DB_CONNECTION=mysql
- DB_HOST=lava_mysql
- DB_PORT=3306
- DB_DATABASE=homestead
- DB_USERNAME=homestead
- DB_PASSWORD=secret

# Migrations & Seeding

- docker-compose exec php php /var/www/artisan migrate
- docker-compose exec php php /var/www/artisan db:seed

# phpMyAdmin

- http://localhost:8183/
- Server: mysql
- Username: homestead
- Password: secret
