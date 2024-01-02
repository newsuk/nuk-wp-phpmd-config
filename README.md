### NUK WP PHPMD config

This library contains PHPMD configuration for NewsUK plugins and themes.

## Installation

Composer install:

```bash
composer require --dev newsuk/nuk-wp-phpmd-config
```

## Using the ruleset
Create a `phpmd.xml.dist` file in your project and add the following:

```xml
<?xml version="1.0"?>
<ruleset>
    <rule ref="vendor/newsuk/nuk-wp-phpmd-config/ruleset.xml" />
</ruleset>
```

## Composer scripts
Add the following to `scripts` section in `composer.json` file to run PHPMD `composer phpmd`.


```json
//Update the file and directory names accordingly
"phpmd": "phpmd nuk-wp-methode.php,includes text phpmd.xml.dist --color"
```

To generate baseline file for existing plugins use `composer phpmd-baseline`

```json
//Update the file and directory names accordingly
"phpmd-baseline": "phpmd nuk-wp-methode.php,includes text phpmd.xml.dist --generate-baseline"
```
