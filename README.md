A fork of the [original TinCanPHP library](https://github.com/RusticiSoftware/TinCanPHP), adapted to query statements from Saltbox's Wax LRS. For details on the problem and the implemented solution, see the [discussion over in the original project](https://github.com/RusticiSoftware/TinCanPHP/pull/17).

[![Build Status](https://travis-ci.org/uOttawaMedtech/TinCanPHP.svg)](https://travis-ci.org/uOttawaMedtech/TinCanPHP)

For hosted API documentation, basic usage instructions, supported version listing, etc. visit the main project website at:

http://rusticisoftware.github.io/TinCanPHP/

For more information about the Tin Can API visit:

http://tincanapi.com/

Requires PHP 5.4 or later. (If you must run something older you should look at the PHP_5_2 branch.)

### Installation

This fork of TinCanPHP is available via [Composer](http://getcomposer.org).

```
php composer.phar require uottawamedtech/tincan:~0.0
```

With the package installed require the Composer autoloader:

```php
require 'vendor/autoload.php';
```

### Testing

Tests are implemented using PHPUnit. Configure the LRS endpoint and credentials by copying the `tests/Config.php.template` to `tests/Config.php` then setting the values for your LRS.

Once configured run:

```
phpunit tests
```

### API Doc Generation

Documentation can be output using [phpDocumentor2](http://phpdoc.org). It will be installed when using Composer. To generate documentation:

```
./vendor/bin/phpdoc.php
```

From the root of the repository after running `php composer.phar update`. Documentation will be output to `doc/api`.

If you do not have the default timezone set in your `php.ini` file you can create one in the base of the repo and use the `PHPRC` environment variable to point to it. Use something like:

```
export PHPRC="/path/to/repos/TinCanPHP/php.ini"
```

And set the timezone in that file using:

```
[PHP]

date.timezone = "US/Central"
```
