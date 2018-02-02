RAD : Builder Service
==========================

[![Latest Stable Version](https://poser.pugx.org/rad/rad-framework-builder/v/stable)](https://packagist.org/packages/rad/rad-framework-builder)
[![Build Status](https://travis-ci.org/guillaumemonet/rad-framework-builder.svg?branch=master)](https://travis-ci.org/guillaumemonet/rad-framework-builder)
[![Total Downloads](https://poser.pugx.org/rad/rad-framework-builder/downloads)](https://packagist.org/packages/rad/rad-framework-builder)
[![Latest Unstable Version](https://poser.pugx.org/rad/rad-framework-builder/v/unstable)](https://packagist.org/packages/rad/rad-framework-builder)
[![License](https://poser.pugx.org/rad/rad-framework/license)](https://packagist.org/packages/rad/rad-framework-builder)
[![Maintainability](https://api.codeclimate.com/v1/badges/7fe5b26b29ba7fd7bd10/maintainability)](https://codeclimate.com/github/guillaumemonet/rad-framework-builder/maintainability)

## Installation

[PHP](https://php.net) 7.1+ and [Composer](https://getcomposer.org) are required.

To get the latest version of RAD Builder Service, simply add the following line to the require block of your `composer.json` file:

```
"rad/rad-framework-builder": "dev-master"
```

## Usage

Put this config in your config.json service template section 

```json

"build": {
    "default": "databasebuilder",
    "classname": "Rad\\Build\\BuildInterface",
    "handlers": {
        "databasebuilder": {
            "classname": "Rad\\Build\\DatabaseBuilderBuildHandler",
            "config": {
                "databaseService": "pdo",
                 "classesPath": "",
                 "controllersPath": ""
            }
        }
    }
}


```

```php
Rad\Build\Build::build();
```




