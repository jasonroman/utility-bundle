Jason Roman's Twig Extension Bundle
==============
[![Build Status](https://travis-ci.org/jasonroman/twig-extension-bundle.svg?branch=master)](https://travis-ci.org/jasonroman/twig-extension-bundle)

This is a class that contains Twig filters.  There are 5 filters:

* *phone* - displays a phone number in a specified format
* *price* - essentially a PHP number_format() clone that adds '$' to the front
* *boolean* - returns 'Yes'/'No' (or custom text) based on the boolean value of the variable
* *md5* - displays the md5 hash of the passed-in value
* *timeAgo* - converts a time to time 'ago', such as 5 days ago, 27 seconds ago, 2 years ago

## Installation

Add the bundle to your `composer.json`

```yaml
{
    "require": {
        "jasonroman/twig-extension-bundle": "1.0.*@dev"
    }
}
```

Register the bundle in ``app/AppKernel.php``

```php
$bundles = array(
    // ...
    new JasonRoman\Bundle\TwigExtensionBundle\JasonRomanTwigExtensionBundle(),
);
```

## Usage

```twig
{{ somePhone|phone }}
{{ someCurrency|price }}
{{ someValue|boolean }}
{{ someString|md5 }}
{{ someDate|timeAgo }}
```