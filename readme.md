# Laravel Administrator

Administrator is an administrative interface builder for [Laravel](http://laravel.com). With Administrator you can visually manage your Eloquent models and their relations, and also create stand-alone settings pages for storing site data and performing site tasks.

- **Author:** Jan Hartigan
- **Website:** [http://Thirdsteplabs.com](http://administrator.Thirdsteplabs.com/)
- **Version:** 4.11.2

[![Build Status](https://travis-ci.org/Thirdsteplabs/Laravel-Administrator.png?branch=master)](https://travis-ci.org/Thirdsteplabs/Laravel-Administrator)

<img src="https://raw.github.com/Thirdsteplabs/Laravel-Administrator/master/examples/images/overview.jpg" />

## Composer

To install Administrator as a Composer package to be used with Laravel 4, simply add this to your composer.json:

```json
"Thirdsteplabs/administrator": "dev-master"
```

..and run `composer update`.  Once it's installed, you can register the service provider in `app/config/app.php` in the `providers` array:

```php
'providers' => array(
    'Thirdsteplabs\Administrator\AdministratorServiceProvider',
)
```

Then publish the config file with `php artisan config:publish Thirdsteplabs/administrator`. This will add the file `app/config/packages/Thirdsteplabs/administrator/administrator.php`. This [config file](http://administrator.Thirdsteplabs.com/docs/configuration) is the primary way you interact with Administrator.

Then finally you need to publish the package's assets with the `php artisan asset:publish Thirdsteplabs/administrator` command.

### Laravel 3

Since Administrator has switched over to Composer, you can no longer use `php artisan bundle:install administrator` or `php artisan bundle:upgrade administrator`. If you want to use Administrator with Laravel 3, you must switch to the [3.3.2 branch](https://github.com/Thirdsteplabs/Laravel-Administrator/tree/3.3.2), download it, and add it in the `/bundles/administrator` directory and add this to your bundles.php file:

```php
'administrator' => array(
    'handles' => 'admin', //this determines what URI this bundle will use
    'auto' => true,
),
```

## Documentation

The complete docs for Administrator can be found at http://administrator.Thirdsteplabs.com. You can also find the docs in the `/src/docs` directory.


## Copyright and License
Administrator was written by Jan Hartigan of Frozen Node for the Laravel framework.
Administrator is released under the MIT License. See the LICENSE file for details.


## Changelog

### 4.11.2
- Bugfix: Strange legacy issue that was never caught with passing a no-op to array_get

### 4.11.1
- Bugfix: There was a routing issue with the new non-numeric model ids

### 4.11.0
- Model ids no longer have to be numeric
- New translations (vi)
