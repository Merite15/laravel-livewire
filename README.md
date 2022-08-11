composer show | grep phpstan

<!-- pint command -->
./vendor/bin/pint

./vendor/bin/pint --test

<!-- add laravel telescope -->
composer require laravel/telescope --dev
php artisan telescope:install


<!-- add phpstan -->
composer require phpstan/phpstan

create a file phpstan.neon for config({
    parameters:

    paths:

        - app

    level: 9

    ignoreErrors:

    excludePaths:
})

./vendor/bin/phpstan analyse

<!-- add larastan -->
composer require nunomaduro/larastan --dev

-add this in phpstan.neon

includes:

    - ./vendor/nunomaduro/larastan/extension.neon

parameters:

    paths:

        - app

    level: 9

    ignoreErrors:

    excludePaths:

<!-- php artisan -->

<!-- add livewire -->
composer require livewire/livewire

<!-- hot refresh with vite -->
add in welcome.blade.php
@vite('resources/js/app.js')

run npm run dev

<!-- Install breeze -->
composer require laravel/breeze --dev
php artisan breeze:install
npm install
npm run dev