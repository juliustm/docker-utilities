# hela-api
Where does all your money go?
If our world was smart enough, this would have been a one second tap, one minuet processing and potential to master your money.

Hussle no more, we are the companion you were waiting. 
A bunch of us are humans like you too. We needed a way to escapable this common challenge by 
1. Collecting receipts smartly
2. Eventualy making receipts smart
3. Offer insightul summary and reports

So we present to you `hela - your receipt companion`
Be it individual, family, group, company, organizations - etc. We have you in mind

# Setting Up
Docker infrastrucre. All necessities are packaged as containers. Follow procedures bellow to setup necessary environment variables and containers.

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