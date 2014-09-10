# Laravel Homestead

The official Laravel local development environment.

Official documentation [is located here](http://laravel.com/docs/homestead?version=4.2).

## Mailcatcher setup
This homestead image also installs [Mailcatcher](http://mailcatcher.me/) for easy mail delivery during local development. 

#### To activate Mailcatcher in your laravel app
Create `app/config/local/mail.php` and add the following:

```php
<?php
// mailcatcher setup
return array(
    'driver' => 'smtp',
    'host' => 'localhost',
    'port' => 1025,
    'encryption' => '',
    'from' => array('address' => 'devmail@mailer.com', 'name' => 'Sender')
);
```

Open up a browser pointing to your homestead box ip and port 10800 (f.e. http://site.dev:10800/) and you have an instant inbox to all mail sent from your app.