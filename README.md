Htmldom
=======

A Htmldom package for Laravel based on Simple HTML Dom Parser.

Link: [Original package](https://github.com/yangqi/Htmldom)

## Installation

Add the following line to the `require` section of `composer.json`:

```bash
composer require jeffreyvr/Htmldom
```

## Setup

Only needed for older Laravel versions.

1. Add the service provider to `config/app.php`.

```php
'providers' => array(
    ...
	'Yangqi\Htmldom\HtmldomServiceProvider',
    ...
```
2. Add alias to `config/app.php`.

```php
'aliases' => array(
    ...
	'Htmldom' => 'Yangqi\Htmldom\Htmldom',
    ...
```

## Usage

1. Use following:

```php
$html = new \Htmldom('http://www.example.com');

// Find all images
foreach($html->find('img') as $element)
       echo $element->src . '<br>';

// Find all links
foreach($html->find('a') as $element)
       echo $element->href . '<br>';
```

See the detailed documentation http://simplehtmldom.sourceforge.net/manual.htm

