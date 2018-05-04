fishmad / wkhtmltopdf-windows
================

This Repo contains the Windows (MinGW-w64) 64-bit Binaries for Windows XP/2003 or later; bundles gcc DLLs.
This version is forked from the github.com/wemersonjanuario/wkhtmltopdf-windows that version relies on VC++ Runtime 2013 and dependencies being installed on the workstation (this package does not and is more independant), so this solution allows me work on my laravel app across multiple windows computers and still use wkhtmltopdf to generate PDF files without needing to install the full wkhtmltopdf package.

[wkhtmltopdf project](http://wkhtmltopdf.org/).
More about the functionality of wkhtmltopdf and wkthmltoimage can be found there.

Binaries for Microsoft Windows using VC++ Runtime 2013, also installable with composer, can be found here: 
[github.com/wemersonjanuario/wkhtmltopdf-windows](https://github.com/wemersonjanuario/wkhtmltopdf-windows)

Binaries for __Linux i386__, also installable with composer, can be found here: [github.com/h4cc/wkhtmltopdf-i386](https://github.com/h4cc/wkhtmltopdf-i386)

Binaries for __Linux amd64__, also installable with composer, can be found here: [github.com/h4cc/wkhtmltopdf-amd64](https://github.com/h4cc/wkhtmltopdf-amd64)

## Use one of these Laravel 5.* PHP packages
[https://github.com/barryvdh/laravel-snappy](https://github.com/barryvdh/laravel-snappy)
OR
[github.com/wemersonjanuario/laravelpdf](https://github.com/wemersonjanuario/laravelpdf)


## Installation
In case this binary package does _not_ work on your work station, try installing the matching operating system packages from here: [http://wkhtmltopdf.org/downloads.html](http://wkhtmltopdf.org/downloads.html).

### Packagist

This package can be found on [Packagist](http://packagist.org) and installed with [Composer](https://getcomposer.org/).

Require the package for Windows with:

    composer require "fishmad/wkhtmltopdf-windows: dev-master"

The binaries will then be located at:

    vendor/fishmad/wkhtmltopdf-windows/bin/64bit

Also a symlink will be created in your configured bin/ folder, for example:

    vendor/bin/32bit/wkhtmltopdf.exe.bat and vendor/bin/64bit/wkhtmltopdf.exe.bat
    
If you choose to use barryvdh/laravel-snappy binary interface wrapper like I have then simply add this line into 
config/snappy.php

    'binary' => base_path('vendor\fishmad\wkhtmltopdf-windows\bin\64bit\wkhtmltopdf.exe'),

    or for a tidier code use a simlinks from above like so:

    'binary' => base_path('vendor\bin\wkhtmltopdf.exe.bat'),
