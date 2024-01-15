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
Add the following to `scripts` section in `composer.json` file and run `composer phpmd`, make sure to update the directory and file names accordingly.

```json
"phpmd": "phpmd plugin.php,includes text phpmd.xml.dist --color"
```

Add the following to generate baseline file for existing plugins and run `composer phpmd-baseline`, make sure to update the directory and file names accordingly.

```json
"phpmd-baseline": "phpmd plugin.php,includes text phpmd.xml.dist --generate-baseline"
```
