(React + Tailwind) && (Inertia + Laravel) Starter Kit

## GETTING STARTED

Clone this repo and then:

```bash
touch .env
```

open the project and paste this into the .env (if it doesn't have one already):

```bash
APP_NAME=Laravel
APP_ENV=local
APP_KEY=base64:lAuqaJRLszhCZUaqn+44h4Eg7hSFHa1Xrh8STpNKpvI=
APP_DEBUG=true
APP_URL=http://localhost

LOG_CHANNEL=stack
LOG_DEPRECATIONS_CHANNEL=null
LOG_LEVEL=debug

DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravel
DB_USERNAME=sail
DB_PASSWORD=password

BROADCAST_DRIVER=log
CACHE_DRIVER=file
FILESYSTEM_DISK=local
QUEUE_CONNECTION=sync
SESSION_DRIVER=file
SESSION_LIFETIME=120

MEMCACHED_HOST=memcached

REDIS_HOST=redis
REDIS_PASSWORD=null
REDIS_PORT=6379

MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
MAIL_USERNAME=null
MAIL_PASSWORD=null
MAIL_ENCRYPTION=null
MAIL_FROM_ADDRESS="hello@example.com"
MAIL_FROM_NAME="${APP_NAME}"

AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=us-east-1
AWS_BUCKET=
AWS_USE_PATH_STYLE_ENDPOINT=false

PUSHER_APP_ID=
PUSHER_APP_KEY=
PUSHER_APP_SECRET=
PUSHER_HOST=
PUSHER_PORT=443
PUSHER_SCHEME=https
PUSHER_APP_CLUSTER=mt1

VITE_PUSHER_APP_KEY="${PUSHER_APP_KEY}"
VITE_PUSHER_HOST="${PUSHER_HOST}"
VITE_PUSHER_PORT="${PUSHER_PORT}"
VITE_PUSHER_SCHEME="${PUSHER_SCHEME}"
VITE_PUSHER_APP_CLUSTER="${PUSHER_APP_CLUSTER}"

```

<br>

### Install Composer (if you've worked with Laravel before, skip this step)
Paste this in your terminal:
```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" <br>
php -r "if (hash_file('sha384', 'composer-setup.php') === '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3') {     echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
```
Run the following in your terminal to move composer into your $PATH
```bash
sudo mv composer.phar /usr/local/bin/composer
```
If you run into any trouble, you can go here and read more: https://getcomposer.org/download/

### Install NPM packages

```bash
npm install
```

### Install composer packages

```bash
composer install
```

### Install Sail (Laravel's built-in Docker config
```bash
php artisan sail:install
```
then type 0 for msyql, press enter <br>

then:
```bash
php artisan key:generate
```

then just to double check run:
```bash
composer update
```

Add sail to your $path (so you can just use 'sail' in future terminal commands):
```bash
alias sail='bash vendor/bin/sail'
```
If you get a "sail command not found" then just re-run this anytime.


## Open Docker Destkop

If you don't have Docker Desktop, you can download it here: https://www.docker.com/products/docker-desktop

Once it's open, run this in your terminal:
```bash
sail up
```
This will start the docker container(s)( If you get a "sail command not found" then you can run -- otherwise skip to the next step): 
```bash
./vendor/bin/sail up
``` 

If you run into any trouble, the Sail documentation is here: https://laravel.com/docs/8.x/sail#introduction

<br>

Open a new tab in the terminal and run:

```bash
sail artisan migrate
```

Or if you're still getting the "sail command not found", run this:

```bash
./vendor/bin/sail artisan migrate
```

For a list of commands you can run, run:
```bash
./vendor/bin/sail artisan
```

Migrations need to be run using 'sail' instead of 'php' so that they are run inside the docker container

Now run:

```bash
npm run dev
```
## Launch 🚀
Main page is here:
```bash
localhost
```

<br>
You'll need a DB client. I like to use TablePlus. <br>
You can download it here: https://tableplus.com/. <br>
<br>
Once you have that downloaded, open it up and click "create a new connection". <br>
Your info should look something like the image below (click "Test" for the boxes to turn green), and then click "Connect":

<img width="504" alt="Screen Shot 2021-05-19 at 10 04 43 PM" src="https://user-images.githubusercontent.com/52245667/118920263-b2bd8900-b8fb-11eb-9db1-8763a66f0d8f.png">

