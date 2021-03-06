# docker-utilities
Useful Docker Containers.

For quickly spinning up a web app/web API

# .env | Environment variables
make a copy of `.env.example > .env`. Note: Change paths and your name to match your directory stucture

# Queworker Configurations
-> ~/docker/queueworker : edit `supervisord.conf` & make a copy of `supervisord.d/template-scheduler.conf.example > template-scheduler.conf`. Note: Change paths to match your directory stucture

# Nginx (site available) Configurations
-> ~/docker/nginx : make a copy of `sites/app.conf.example > app.conf`. Note: Change paths to match your directory stucture

# Starting containers
$ docker-compose up -d OR $ docker-compose up -d nginx elasticsearch ( Specify Container names based on docker-compose.yml names)

# Installing laravel framework and other PHP frameworks/libraries
$ docker exec -it boilerplat_workspace_1 bash ( `boilerplate` is a placeholder for your respective stack name )
$ cd into your project directory ( i.e docker-utilities )
$ composer global require laravel/installer
$ composer create-project --prefer-dist laravel/laravel:^7.0 blog

Read more here : https://laravel.com/docs/7.x/installation


Laravel Configuration - Public Directory

After installing Laravel, you should configure your web server's document / web root to be the public directory. The index.php in this directory serves as the front controller for all HTTP requests entering your application.

Configuration Files

All of the configuration files for the Laravel framework are stored in the config directory. Each option is documented, so feel free to look through the files and get familiar with the options available to you.

Directory Permissions

After installing Laravel, you may need to configure some permissions. Directories within the storage and the bootstrap/cache directories should be writable by your web server or Laravel will not run. If you are using the Homestead virtual machine, these permissions should already be set.

Application Key

The next thing you should do after installing Laravel is set your application key to a random string. If you installed Laravel via Composer or the Laravel installer, this key has already been set for you by the php artisan key:generate command.

Typically, this string should be 32 characters long. The key can be set in the .env environment file. If you have not copied the .env.example file to a new file named .env, you should do that now. If the application key is not set, your user sessions and other encrypted data will not be secure!

Additional Configuration

Laravel needs almost no other configuration out of the box. You are free to get started developing! However, you may wish to review the config/app.php file and its documentation. It contains several options such as timezone and locale that you may wish to change according to your application.

You may also want to configure a few additional components of Laravel, such as:

Cache
Database
Session