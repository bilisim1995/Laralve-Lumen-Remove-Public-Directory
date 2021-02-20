# Laravel-Lumen-Remove-Public-Directory
How to remove public directory laravel/lumen

<br>

### Version :monocle_face:
php artisan --version


```
Laravel Framework Lumen (8.2.1) (Laravel Components ^8.0)
```
<br><br><hr>

## Public Directory
When we first install the lumen, the default folder/route is set to public. ```http:example.com/public```. When we want to remove the public directory on the project, we can follow the steps below.
<br><br><br>

# Step 1:
We move the .htaccess and index.php files in the public folder to the main directory.
<br><br><br>

# Step 2:
Change index.php
```
$app = require __DIR__.'/../bootstrap/app.php';
```
to
```
$app = require __DIR__.'/bootstrap/app.php';
```
<br><br><br>

# Step 3:
create file ```home.blade.php``` in resources/views/ 
<br><br><br>

# Step 4:
add this code in routes/web.php
```
$router->get('/', function () {
    return view('home');
});
```
<br><br><br>

### :partying_face: :ok_hand: Done. now the main project directory is not public. http://example.com/
