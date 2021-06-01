# Laravel Credit Card Validator


Adds some minimal validation rules for credit card.

This fork from original author rap2hpoutre/laravel-credit-card-validator is to support php 7.4 as there are issues

## Install
Install via composer
```
composer require selay/laravel-credit-card-validator
```
Add Service Provider to `config/app.php` in `providers` section
```php
Rap2hpoutre\LaravelCreditCardValidator\ServiceProvider::class,
```

## Usage

Add this to your validation rules:

```php
// Add this in your controller method
$this->validate($request, [
    'credit-card-number' => 'required|ccn',
    'credit-card-date' => 'required|ccd',
    'credit-validation-code' => 'required|cvc',
]);
```
