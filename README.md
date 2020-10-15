# docker

# Install Docker 
- Windows: https://docs.docker.com/docker-for-windows/install/
- Linux: https://docs.docker.com/engine/install/ubuntu/
- Mac: https://docs.docker.com/docker-for-mac/install/

# Spin containes
- Run following command to spin all containers: 
  - docker-compose up -d
    
# Start Laravel project
- Clone Laravel project to src/ directory
  - git clone https://github.com/Renfos/Lavalite.git src
- cd src/ folder
- composer install
- npm install
- npm run dev
- cp .env.example .env

# Update Laravel DB credentials
- DB_CONNECTION=mysql
- DB_HOST=mysql_lava
- DB_PORT=3306
- DB_DATABASE=homestead
- DB_USERNAME=homestead
- DB_PASSWORD=secret

# Migrations & Seeding
- docker-compose exec php php /var/www/artisan migrate
- docker-compose exec php php /var/www/artisan db:seed

