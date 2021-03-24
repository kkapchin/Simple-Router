#Usage
###1. As first step add the path to your page 404 controller:
```php
Route::page404(string $path);
```

###2. Add url-link and controller path. Very simple. Repeat this step as much as many routes you need.
```php
Route::path(string $url)->component(string $controller_path);
Route::path(string $url)->component(string $controller_path);
Route::path(string $url)->component(string $controller_path);
```
###3. Next step you need to add the closing line:
```php
Route::start();
```
###4. Eventually the whole structure should look like in example below:
```php
Route::page404('../controllers/page404.php');
    Route::path('/')->component('../controllers/homepage.php');
    Route::path('/homepage')->component('../controllers/homepage.php');
    Route::path('/about')->component('../controllers/about.php');
    Route::path('/messenger')->component('../controllers/messenger.php');
    Route::path('/news')->component('../controllers/newsfeed.php');
Route::start();
```
