# nuk-wp-phpmd-config

This library contains PHPMD configuration for NewsUK plugins and themes.

## Architecture

### Project Structure

```text
- .circleci          # CircleCI pipeline configuration files
- .github            # GitHub configuration files
- ruleset.xml        # PHPMD rulesets
```

## Technical Documentation

-   [Package Extensibility](docs/extensibility.md)

## Contribution

More details on how to contribute to this package can be found in the [CONTRIBUTING.md](docs/CONTRIBUTING.md) file.

### Minimal requirements

-   PHP 8.2

## Development setup

To build the package

PHP setup

-   `composer install`

## Installation

Composer install:

```bash
composer require --dev newsuk/nuk-wp-phpmd-config
```

## Usage

### Using the ruleset

Create a `phpmd.xml.dist` file in your project and add the following:

```xml
<?xml version="1.0"?>
<ruleset>
    <rule ref="vendor/newsuk/nuk-wp-phpmd-config/ruleset.xml" />
</ruleset>
```

### Usage with Composer
Add the following to `scripts` section in `composer.json` file and run `composer phpmd`, make sure to update the directory and file names accordingly.

```json
"phpmd": "phpmd plugin.php,includes text phpmd.xml.dist --color"
```

Add the following to generate baseline file for existing plugins and run `composer phpmd-baseline`, make sure to update the directory and file names accordingly.

```json
"phpmd-baseline": "phpmd plugin.php,includes text phpmd.xml.dist --generate-baseline"
```

## Tagging and releasing

The content schema uses Semantic Versioning `semver` for versioning. The package is released using [GitHub Releases](https://docs.github.com/en/github/administering-a-repository/releasing-projects-on-github/about-releases). The release process is automated in Circle CI build step. To create a new release, follow these steps:

-   Update the relevant files with the new version. Commit the updated files.
-   Push the changes to the `main` branch, by merging the associated pull request
-   Create a release targeting the `main` branch within GitHub.
