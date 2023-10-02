 
[Documentation](http://open-admin.org/docs/en/extension-api-tester)

## Screenshot

![extention-api-tester](https://user-images.githubusercontent.com/86517067/153463990-bd59e3ac-bc88-4858-adac-2714cc08e705.png)


## Installation

```
$ composer require snowsoft/oaapi-tester

$ php artisan vendor:publish --tag=api-tester

```

Then last run flowing command to import menu and permission:

```
$ php artisan admin:import api-tester
```

Finally open `http://localhost/admin/api-tester`.

## Configuration

`api-tester` supports 3 configuration, open `config/admin.php` find `extensions`:
```php

    'extensions' => [

        'api-tester' => [

            // route prefix for APIs
            'prefix' => 'api',

            // auth guard for api
            'guard'  => 'api',

            // If you are not using the default user model as the authentication model, set it up
            'user_retriever' => function ($id) {
                return \App\User::find($id);
            },
        ]
    ]

```

License
------------
Licensed under [The MIT License (MIT)](LICENSE).
