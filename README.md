<h3 align="center">Build scalable marketplace faster | With PHP 8.0 and Laravel 9.0</h3>

<a name="Introduction"></a>

**Agora** is an Apiato open source marketplace platform.

<a name="Setup"></a>

## Project setup with Docker

1. Install Docker (**for ubuntu**)
   1. Install docker using `sudo apt install docker.io` command.
   2. Install all the dependency packages using `sudo snap install docker` command.
2. Run project
   1. Fork the project
   2. Clone the project using `git clone REPO_ADDRESS` command
   3. Create .env from .env.example using `cp .env.example .env`
   4. Modify `DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD` inside the .env file
   5. Build containers for services of the entire app using `docker compose up -d --build`
   6. Get 'agora-db' container ID using `docker ps`
   7. Get container IP Address using `docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' CONTAINER_ID`
   8. Replace the IP Address of step 7 by `DB_HOST` of env file
   9. Get a shell on the agora-app container using `docker exec -it agora-app bash`
   10. Install packages `composer install`
   11. Generate APP_KEY using `php artisan key:generate`
   12. Migrate and seed `php artisan migrate --seed`
   13. Create encryption keys needed to generate secure access token using `php artisan passport:install`
   14. Open up your web browser and type [127.0.0.1:8000](http://127.0.0.1:8000) into the address bar, then press Enter.

<a name="Contributors"></a>

## Contributing

Feel free to dive in! Fix open [Issues](https://github.com/laravel-tech/agora/issues/) and submit new [features](https://github.com/laravel-tech/agora/pulls?q=is%3Apr+is%3Aopen+sort%3Aupdated-desc).
<br>
Agora follows the [Contributor Covenant](https://www.contributor-covenant.org/version/1/4/code-of-conduct) Code of Conduct.

<a name="License"></a>
## License

[MIT](https://github.com/laravel-tech/agora/blob/master/LICENSE) © Mj Pakzad
