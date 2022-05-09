# composer-versions-check

composer-versions-check is a plugin for Composer.

It warns user for outdated packages from last major versions after update command.

[![Latest Version on Packagist](https://img.shields.io/packagist/v/stepanenko3/composer-versions-check.svg?style=flat-square)](https://packagist.org/packages/stepanenko3/composer-versions-check)
[![Total Downloads](https://img.shields.io/packagist/dt/stepanenko3/composer-versions-check.svg?style=flat-square)](https://packagist.org/packages/stepanenko3/composer-versions-check)
[![License](https://poser.pugx.org/stepanenko3/composer-versions-check/license)](https://packagist.org/packages/stepanenko3/composer-versions-check)

![composer-versions-check_demo](https://cloud.githubusercontent.com/assets/1698357/14637529/2e32a778-0632-11e6-99c7-0e1c284a7436.gif)

## Installation

You can install it either globally (recommended):

```bash
composer global require stepanenko3/composer-versions-check
```

or locally (as require-dev dependency then):

```bash
composer require --dev stepanenko3/composer-versions-check
```

## Usage

That's it! Composer will enable automatically the plugin as soon it's installed.

Just run `composer update` command to see the plugin working.

## Configuration

You can configure the plugin via the [`COMPOSER_HOME/config.json`](https://getcomposer.org/doc/03-cli.md#composer-home) file. Here is the default one:

```json
{
    "config": {
        "stepanenko3-composer-versions-check": {
            "root-packages-only": false,
            "show-links": false,
            "vendor": "laravel"
        }
    }
}
```

* `ignore-sub-dependencies`: Shows only outdated root packages.
* `show-links`: Shows outdated package links. Set to `true` to get a larger output, like the demo.
* `vendor`: Limits the output to a specific vendor/provider.
