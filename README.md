# CodeIgniter HTMX Demo

This is a demo for [CodeIgniter HTMX](https://github.com/michalsn/codeigniter-htmx) helper library.

## Installation

To easily play with the code, you're supposed to download the package and install it manually.

Download this project and place it in the desired folder. The example will assume that it will be `app/ThirdParty/htmx-demo`. Then enable it by editing the `app/Config/Autoload.php` file and adding the `Michalsn\CodeIgniterDemoHtmx` namespace to the `$psr4` array, like in the below example:

```php
<?php

...

public $psr4 = [
    APP_NAMESPACE => APPPATH, // For custom app namespace
    'Config'      => APPPATH . 'Config',
    'Michalsn\CodeIgniterDemoHtmx' => APPPATH . 'ThirdParty/htmx-demo/src',
];

...
```

## Database

Before running the examples you have to migrate the database. Make sure you have set all the credentials to the database and then you can run the command:
```console
php spark migrate --all
```

And preferably run the seeds:

**For Unix:**
```console
php spark db:seed Michalsn\\CodeIgniterDemoHtmx\\Database\\Seeds\\SeedDemo
```

**For Windows:**
```console
php spark db:seed Michalsn\CodeIgniterDemoHtmx\Database\Seeds\SeedDemo
```

## Running the demo

The default route to the demo page is `demo`.