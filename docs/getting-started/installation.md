---
title: Installation
order: 1
---

# Installation

You can install Laravel API Documentation Generator using composer:

```bash
composer require codise/laravel-apidoc-generator
```

## Laravel
Publish the config file by running:

```bash
php artisan vendor:publish --provider="Codise\ApiDoc\ApiDocGeneratorServiceProvider" --tag=apidoc-config
```
This will create an `apidoc.php` file in your `config` folder.

## Lumen
Register the service provider in your `bootstrap/app.php`:

```php
$app->register(\Codise\ApiDoc\ApiDocGeneratorServiceProvider::class);
```

Next, copy the config file from `vendor/codise/laravel-apidoc-generator/config/apidoc.php` to your project as `config/apidoc.php`. 

Then add to your `bootstrap/app.php`:

```php
$app->configure('apidoc');
```
