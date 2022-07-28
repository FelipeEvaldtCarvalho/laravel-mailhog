
# MailHog with Laravel

This is a small setup to help using the MailHog with an older version of Laravel using the docker container, I hope it will be helpful.


# Building

After cloning this repository, build the mailhog container with:

```
docker-compose up -d
```
or
```
make up
```

# Connecting containers network

```
docker network connect laravel-mailhog_laravel_mailhog_network <PHP-CONTAINER-NAME>
```
Command example:

```
docker network connect laravel-mailhog_laravel_mailhog_network php7_develop
```

# Access panel

Go to http://localhost:8100, to use the Mailhog Panel

# Change variables in your Laravel .env

```
MAIL_MAILER=smtp
MAIL_HOST=mailhog
MAIL_PORT=1025
MAIL_USERNAME=''
MAIL_PASSWORD=''
MAIL_ENCRYPTION=null
```

# More information:

https://github.com/mailhog/MailHog