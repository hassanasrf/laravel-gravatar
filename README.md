# Implement Gravatar Image using thomaswelton/laravel-gravatar
###### Gravatar is a service that provide unique globally avatars and integrated it into their WordPress.com blogging platform. If you don't have avatar image then you can get Gravatar src image from thier email if it register on WordPress.com. So if you want to implement in your laravel application then it is very easy. There are several package for Gravatar image for laravel, but we will use thomaswelton/laravel-gravatar package that is i think better.

### First fire following command on your terminal.
###### Installation Package
```php
composer require thomaswelton/laravel-gravatar
```

###### After install this package, Now open config/app.php file and add service provider and aliase.
### config/app.php

```php
'providers' => [
	....
	Thomaswelton\LaravelGravatar\LaravelGravatarServiceProvider::class,
],
'aliases' => [
	....
	'Gravatar' => Thomaswelton\LaravelGravatar\Facades\Gravatar::class
],
```

###### now we can use Gravatar in our blade file like this way:
### Use In Blade File
```php
<img src="{{ Gravatar::src('your@email.com', 200) }}">
```
