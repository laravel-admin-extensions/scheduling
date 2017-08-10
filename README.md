laravel-admin-ext/scheduling
============================

A web interface for manage task scheduling in laravel.

## Screenshot

![wx20170810-101048](https://user-images.githubusercontent.com/1479100/29151552-8affc0b2-7db4-11e7-932a-a10d8a42ec50.png)

## Installation

```
$ composer require laravel-admin-ext/scheduling


$ php artisan admin:import scheduling
```

Open `http://your-host/admin/scheduling`.

Try to add a scheduling task in `app/Console/Kernel.php` like this:

```php
class Kernel extends ConsoleKernel
{
    protected function schedule(Schedule $schedule)
    {
        $schedule->command('inspire')->everyTenMinutes();
        
        $schedule->command('route:list')->dailyAt('02:00');
    }
}

```

And you can find these tasks in scheduling panel.

License
------------
Licensed under [The MIT License (MIT)](LICENSE).
