## Laravel API Documentation Generator

Automatically generate your API documentation from your existing Laravel/Lumen/[Dingo](https://github.com/dingo/api) routes.

`php artisan apidoc:generate`

## Installation
PHP 7.2 and Laravel/Lumen 5.7 or higher are required.

> If your application does not meet these requirements, you can check out the 3.x branch for older releases.

```sh
composer require --dev desmart/laravel-apidoc-generator
```

### Laravel
Publish the config file by running:

```bash
php artisan vendor:publish --provider="Mpociot\ApiDoc\ApiDocGeneratorServiceProvider" --tag=apidoc-config
```

This will create an `apidoc.php` file in your `config` folder.

### Lumen
- When using Lumen, you will need to run `composer require desmart/laravel-apidoc-generator` instead.
- Register the service provider in your `bootstrap/app.php`:

```php
$app->register(\Mpociot\ApiDoc\ApiDocGeneratorServiceProvider::class);
```

- Copy the config file from `vendor/desmart/laravel-apidoc-generator/config/apidoc.php` to your project as `config/apidoc.php`. Then add to your `bootstrap/app.php`:

```php
$app->configure('apidoc');
```

## Documentation
Check out the documentation at the [Beyond Code homepage](https://beyondco.de/docs/laravel-apidoc-generator/).

### License

The Laravel API Documentation Generator is free software licensed under the MIT license.
