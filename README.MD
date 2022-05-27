#  validation lib

validation is a small php validation lib for mysql databases.

## installation

install once with composer:

```
composer require itsharks/validation
```

then add this to your project:

```php
require_once "vendor/autoload.php";

$validation = new \Itsharks\Validation\validation();
```

## usage

```php

/* required */
$validation->input("inputname")->required();
/* email */
$validation->input("inputname")->email();
/* min */
$validation->input("inputname")->min(number);
/* max */
$validation->input("inputname")->max(number);

// show errors 
$validation->showErorr();

// is error 
$validation->is_error();

// case 
$validation->input("inputname")->required()->min(2)->max(10);
$validation->showErorr();
if($validation->is_error()){
    // statement   
}


```

