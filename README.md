# php-crawler

A crawler application written with php and Laravel that finds email addresses on the internets.
Given an entry point url, the crawler will search for emails in all the urls available from this entry point domain name.
The emails are downloadable in a text file at any time.
Several users can start searching for emails without viewing the other users' searches (searches are related to a user).

## Server requirements

- PHP >= 7.2.0
- OpenSSL PHP Extension
- PDO PHP Extension
- Mbstring PHP Extension
- Tokenizer PHP Extension
- XML PHP Extension

## Installation

- Create a mysql database (default name: `crawler`)
- Install the project with [composer](https://getcomposer.org/):
```bash
composer create-project hedii/php-crawler crawler
cd crawler
```
- Open the `.env` file, check the database credentials, and modify it if needed:
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=crawler
DB_USERNAME=root
DB_PASSWORD=your_password_here
```
- Build the crawler application
```bash
php artisan crawler:build
```
- Point your web server's document / web root to be the public directory: `/some/path/crawler/public`. The index.php in this directory serves as the front controller for all HTTP requests entering your application. [See Laravel documentation](https://laravel.com/docs/master/installation). If highly recommend using [Laravel Valet](https://laravel.com/docs/master/valet) if you are using a Mac. Otherwise, check [Laravel Homestead](https://laravel.com/docs/master/homestead)
- Done

## Usage

- Navigate to your php-crawler website
- Register a new account
- Create a new search
- Create more searches
- Download the found emails

## Testing

```
composer test
```

## Contributing

**All** contributions are welcome :)

Please write some tests if you are adding or modifying features.

## License

php-crawler is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
