# Admin LTE Control Panel and Laravel 5

This Package adds latest version of AdminLTE Control Panel and some extra features in your Fresh Laravel 5 installation.

## Extra Features

*   Auth Views
*   Localization on views and functionality
*   Global file for Project Company Data.
*   More Features Coming Soon.

## Installation

type in console:
```
composer require edujugon/adminlte
```

## Laravel 5.*

Register AdminLTE service by adding it to the providers array.

    'providers' => array(
        ...
        Edujugon\AdminLTE\Providers\AdminLTEServiceProvider::class
    )

## Recommended Steps

Since this package integrates auth views you should set up the Laravel Authentication Feature first:

Just run the following commands in your fresh Laravel application:

*   `php artisan make:auth` 

Then 

*   `php artisan migrate`


## Publish AdminLTE Dependencies

>Since you will typically need to overwrite the dependencies every time the package is updated, I recommend to use the --force flag.

```
php artisan vendor:publish --tag=adminLTE_dependencies --force
```

## Publish Views

Publish the package's view files to the application's own view directory

```
php artisan vendor:publish --tag=adminLTE_views --force
```

## Publish Language Files and Controller.

Publish the package's language files to the application's own lang directory.

Publish the package's LanguageController file to the application's own Controllers directory

### Current Languages
 
*   English
*   Spanish
*   More Languages coming soon

```
php artisan vendor:publish --tag=adminLTE_languages
```

The last step is to add the below line to project's routes file.

#### Laravel 5.3

File: routes/web.php

#### Minor than 5.3

File: app/routes.php

```
Route::get('language/{lang}', 'LanguageController@index');
```

## Publish Company parameters File.

It will publish a file where you may have all project company data in one place.

File Location: config/company.php

```
php artisan vendor:publish --tag=adminLTE_config
```



## AdminLTE Control panel Preview and Documentation

[https://almsaeedstudio.com/](https://almsaeedstudio.com/)