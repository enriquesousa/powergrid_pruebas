# Laravel Livewire: Crea DataTables en Minutos con Powergrid
https://www.youtube.com/watch?v=sV6Rs2y8fWk

## En Homestead.yaml
```php
sites:
    - map: homestead.pruebas.powergrid
      to: /home/vagrant/code/pruebas/powergrid/public

databases:
    - powergrid
```

## Modificar:
- sudo micro /etc/hosts
- sudo service network-manager restart

## Si le hacemos algún cambio a Homestead.yaml:
- vagrant reload --provision

- vagrant up (Start VM)
- vagrant ssh (Enter VM)
- vagrant halt (Stop VM)

## PowerGrid
https://livewire-powergrid.com/#/get-started/powergrid

## Start Project
- laravel new powergrid --jet

## Install via composer
Require PowerGrid via Composer, run:
- composer require power-components/livewire-powergrid

Publish PowerGrid configuration file. Run the following command:
- php artisan vendor:publish --tag=livewire-powergrid-config

skip this step if you don’t need to customize views or language files. To publish Views, run:
- php artisan vendor:publish --tag=livewire-powergrid-views

Copy to clipboardErrorCopied
To publish Language files, run:
- php artisan vendor:publish --tag=livewire-powergrid-lang

Styles must be included before the </head> tag.
```php
 <!-- Styles -->
    @livewireStyles
    @powerGridStyles

   </head>
```

Copy to clipboardErrorCopied
Scripts must be included before the </body> tag.
```php
 <!-- Scripts -->
    @livewireScripts
    @powerGridScripts

</body>
```

For Tailwind 3.x - read
```php
module.exports = {
  content: [
      // ....
      './app/Http/Livewire/**/*Table.php',
      './vendor/power-components/livewire-powergrid/resources/views/**/*.php',
      './vendor/power-components/livewire-powergrid/src/Themes/Tailwind.php'
  ]
  // ....
}
```

If you use Tailwind forms, please consider modifying your tailwind.config.js to use the strategy class as follows:
```php
module.exports = {
   //...
  plugins: [
    require("@tailwindcss/forms")({
      strategy: 'class',
    }),
  ]
}
```

Compilar:
- npm run dev

Crear el Git repo:
- git init

3:40
Crear la tabla
