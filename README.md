# Backpack Generators

[![Latest Version on Packagist](https://img.shields.io/packagist/v/backpack/generators.svg?style=flat-square)](https://packagist.org/packages/backpack/generators)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://img.shields.io/travis/laravel-backpack/generators/master.svg?style=flat-square)](https://travis-ci.org/laravel-backpack/generators)
[![Coverage Status](https://img.shields.io/scrutinizer/coverage/g/laravel-backpack/generators.svg?style=flat-square)](https://scrutinizer-ci.com/g/laravel-backpack/generators/code-structure)
[![Quality Score](https://img.shields.io/scrutinizer/g/laravel-backpack/generators.svg?style=flat-square)](https://scrutinizer-ci.com/g/laravel-backpack/generators)
[![Style CI](https://styleci.io/repos/53490941/shield)](https://styleci.io/repos/53490941)
[![Total Downloads](https://img.shields.io/packagist/dt/backpack/generators.svg?style=flat-square)](https://packagist.org/packages/backpack/generators)

Quickly generate Backpack templated Models, Requests, Views and Config files for projects using Backpack for Laravel as their admin panel.


## Install

Via Composer

``` bash
composer require jkg/backpack-generators 
```

``` bash
php artisan backpack:install
```


## Usage

Open the console and enter one of the commands:


- **Generate Backpack\CRUD interfaces for all Eloquent models that don't already have one:**

```bash
php artisan backpack:build
```

- **Generate all files for one new Backpack\CRUD interface:**

``` bash
php artisan backpack:crud {Entity_name}

# Use singular, either PascalCase, snake_case or kebab-case.
# This will create a Model if there isn't one, or add
# our CrudTrait to the model if it already exists.
```

- **Generate all files for a custom admin panel page:**

``` bash
php artisan backpack:page {PageName}

# You can use either PascalCase, snake_case or kebab-case.
# This will generate you a Controller, a view and a route.
```

- Generate a new Backpack\CRUD file:
``` bash
php artisan backpack:crud-controller {Entity_name}
php artisan backpack:crud-model {Entity_name}
php artisan backpack:crud-request {Entity_name}
```

- Generate a model (available options: --softdelete)

``` bash
php artisan backpack:model {Entity_name}
```

- Generate a request

``` bash
php artisan backpack:request {Entity_name}
```

- Generate a view (available options: --plain)

``` bash
php artisan backpack:view {Entity_name}
``` 

- Generate a config file

``` bash
php artisan backpack:config {Entity_name}
```

- Generate a button

``` bash
php artisan backpack:button {button_name}
```

- Generate a field

``` bash
php artisan backpack:field {field_name}

// or generate a field starting from another field
php artisan backpack:field {field_name} --from={original_field_name}
```

- Generate a column

``` bash
php artisan backpack:column {column_name}

// or generate a column starting from another column
php artisan backpack:column {column_name} --from={original_column_name}
```

- Generate a filter

``` bash
php artisan backpack:filter {filter_name}

// or generate a filter starting from another filter
php artisan backpack:filter {filter_name} --from={original_filter_name}
```

- Generate a widget

``` bash
php artisan backpack:widget {widget_name}

// or generate a widget starting from another widget
php artisan backpack:widget {widget_name} --from={original_widget_name}
```
