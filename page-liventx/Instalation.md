## Documentación de instalación de Page LiventX

### Requisitos

* PHP ^7.2.5
* MySQL 5.6 o superior
* Composer
* NodeJS
* NPM

### Instalación

1. Clonar el repositorio de GitHub
2. Instalar las dependencias de PHP con Composer
3. Instalar las dependencias de NodeJS con NPM
4. Crear la base de datos
5. Configurar el archivo .env
6. Correr el servidor de desarrollo

#### Clonar el repositorio de GitHub

Para clonar el repositorio de GitHub, ejecutar el siguiente comando:

    git clone https://{user}@bitbucket.org/inmovdev/page-liventx.git

#### Instalar las dependencias de PHP con Composer

Para instalar las dependencias de PHP con Composer, ejecutar el siguiente comando:

    composer install

Si requiere instalar Composer, puede hacerlo desde el siguiente enlace: [https://getcomposer.org/download/](https://getcomposer.org/download/)

Si necesita update de las dependencias, ejecutar el siguiente comando:

    composer update

#### Instalar las dependencias de NodeJS con NPM

Para instalar las dependencias de NodeJS con NPM, ejecutar el siguiente comando:

    npm install

Si requiere instalar NodeJS, puede hacerlo desde el siguiente enlace: [https://nodejs.org/es/download/](https://nodejs.org/es/download/)

#### Configurar el archivo .env

Copiar el archivo .env.example a .env y configurar los datos de conexión a la base de datos.

#### Correr el servidor de desarrollo

Para correr el servidor de desarrollo, ejecutar el siguiente comando:

    php artisan serve

### Instalación en producción

#### Instalar PHP

    sudo yum install php72 php72-mysqlnd php72-mbstring php72-xml php72-gd php72-mcrypt php72-mbstring php72-mysqlnd php72-opcache php72-pdo php72-pecl-imagick php72-pecl-memcached php72-pecl-redis php72-pecl-zip php72-process php72-soap php72-xml php72-zip

#### Instalar Composer

    curl -sS https://getcomposer.org/installer | php
    sudo mv composer.phar /usr/local/bin/composer

#### Instalar NodeJS

    curl -sL https://rpm.nodesource.com/setup_10.x | sudo bash -
    sudo yum install nodejs

#### Instalar MySQL

    sudo yum install mysql57-server
    sudo service mysqld start
    sudo /usr/bin/mysql_secure_installation

#### Instalar Nginx

    sudo yum install nginx

#### Configurar Nginx

    sudo vi /etc/nginx/nginx.conf

Agregar la siguiente configuración:

    server {
        listen 80;
        server_name name;
        root /var/www/html/name/public;
        index index.php index.html index.htm;
        location / {
            try_files $uri $uri/ /index.php?$query_string;
        }
        location ~ \.php$ {
            try_files $uri /index.php =404;
            fastcgi_split_path_info ^(.+\.php)(/.+)$;
            fastcgi_pass
            fastcgi_index index.php;
            fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
            include fastcgi_params;
        }
    }

#### Configurar PHP

    sudo vi /etc/php.ini

Agregar la siguiente configuración:

    date.timezone = America/Mexico_City

#### Configurar MySQL

    sudo vi /etc/my.cnf

Agregar la siguiente configuración:

    [mysqld]
    character-set-server=utf8mb4
    collation-server=utf8mb4_unicode_ci
    [client]
    default-character-set=utf8mb4
    [mysql]
    default-character-set=utf8mb4

#### Configurar el archivo .env

Copiar el archivo .env.example a .env y configurar los datos de conexión a la base de datos.

#### Instalar las dependencias de PHP con Composer

    composer install   

#### Instalar las dependencias de NodeJS con NPM

    npm install
 
#### Configurar el archivo .htaccess

    sudo vi /var/www/html/page-liventx/public/.htaccess

Agregar la siguiente configuración:

    RewriteEngine On
    RewriteCond %{REQUEST_FILENAME} !-d
    RewriteCond %{REQUEST_FILENAME} !-f
    RewriteRule ^ index.php [L]
    
#### Correr el servidor de producción

    php artisan serve --host= name --port=80 --env=production

