laravel-admin-ext/scheduling
============================

A web interface for manage task scheduling in laravel.

## Installation

```
$ composer require laravel-admin-ext/scheduling

```

Open `app/Providers/AppServiceProvider.php`, and call the `Scheduling::boot` method within the `boot` method:

```php
<?php

namespace App\Providers;

use Encore\Admin\Scheduling\Scheduling;
use Illuminate\Support\ServiceProvider;

class AppServiceProvider extends ServiceProvider
{
    public function boot()
    {
        Scheduling::boot();
    }
}
```

then run: 

```
$ php artisan admin:import scheduling
```

Open `http://your-host/admin/scheduling`.

License
------------
Licensed under [The MIT License (MIT)](LICENSE).
