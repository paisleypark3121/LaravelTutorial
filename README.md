# LaravelTutorial

https://engineering.paiza.io/entry/paizacloud_laravel

Create an account at paiza cloud
After created a new "server" enter terminal and type:
$ laravel new MYAPPNAME

then enter MYAPPNAME folder:
$ cd myapp
$ php artisan serve

clicking the we browser on the left it will be opened the main PAGE located at:
MYAPPNAME/resources/views/welcome.blade.php

inside MYAPPNAME/App/Http/Controllers we can find the "controller.php"

inside MYAPPNAME/Routes there's "web.php" which contains the route to the View:

Route::get('/', function () {
    return view('welcome');
});

this refers to: resources/view/welcome.blade.php

Let us now understand the steps involved in routing mechanism in detail −
- Step 1 − Initially, we should execute the root URL of the application.
- Step 2 − Now, the executed URL should match with the appropriate method in the route.php file. In the present case, it should match the method and the root (‘/’) URL. This will execute the related function.
- Step 3 − The function calls the template file resources/views/welcome.blade.php. Next, the function calls the view() function with argument ‘welcome’ without using the blade.php.

Example with routed ID:
Route::get('ID/{id}',function($id) {
   echo 'ID: '.$id;
});

Optional parameter:
Route::get('user/{name?}', function ($name = 'This is a "Default Name"') 
{ 
    return 'Hello '.$name;
});

In order to create a new controller:
php artisan make:controller <controller-name>
