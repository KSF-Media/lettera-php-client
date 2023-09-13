# lettera

<h2>KSF Media's articles service</h2> Changelog for V3: <ul><li>Unified <code>ListArticle</code> and <code>RelatedArticle</code> into a single type <code>ArticleStub</code>. NOTE: In contrast to the old types, <code>ArticleStub.relatedArticles</code> is now an optional value.</li> <li>Added endpoint <code>/article/{uuid}/stub</code></li> <li>Removed deprecated endpoint <code>/article/search</code></li> </ul>

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 3.0.0
- Build package: org.openapitools.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/KSF-Media/lettera-php-client.git"
    }
  ],
  "require": {
    "KSF-Media/lettera-php-client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/lettera/vendor/autoload.php');
```

## Tests

To run the unit tests:

```bash
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\ArticlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$uuid = 'uuid_example'; // string | 
$auth_user = 'auth_user_example'; // string | 
$authorization = 'authorization_example'; // string | 
$x_real_ip = 'x_real_ip_example'; // string | 
$textonly = false; // bool | 

try {
    $result = $apiInstance->articleUuidGet($uuid, $auth_user, $authorization, $x_real_ip, $textonly);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articleUuidGet: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *http://http:/v3*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ArticlesApi* | [**articleUuidGet**](docs/Api/ArticlesApi.md#articleuuidget) | **GET** /article/{uuid} | 
*ArticlesApi* | [**articleUuidStubGet**](docs/Api/ArticlesApi.md#articleuuidstubget) | **GET** /article/{uuid}/stub | 
*CategoriesApi* | [**categoriesGet**](docs/Api/CategoriesApi.md#categoriesget) | **GET** /categories | Read categories
*ListsApi* | [**frontpageGet**](docs/Api/ListsApi.md#frontpageget) | **GET** /frontpage | Returns a list for a front page
*ListsApi* | [**latestGet**](docs/Api/ListsApi.md#latestget) | **GET** /latest | Returns a list of latest articles
*ListsApi* | [**mostreadGet**](docs/Api/ListsApi.md#mostreadget) | **GET** /mostread | Returns a list of most read articles
*ListsApi* | [**presetPresetCategoryGet**](docs/Api/ListsApi.md#presetpresetcategoryget) | **GET** /preset/{preset}/{category} | Load a preset model
*ListsApi* | [**presetPresetCategoryPost**](docs/Api/ListsApi.md#presetpresetcategorypost) | **POST** /preset/{preset}/{category} | Update a preset model
*ListsApi* | [**searchGet**](docs/Api/ListsApi.md#searchget) | **GET** /search | Returns a list of search results
*ListsApi* | [**tagTagGet**](docs/Api/ListsApi.md#tagtagget) | **GET** /tag/{tag} | Returns a list of latest articles by tag


## Documentation For Models

 - [Alignment](docs/Model/Alignment.md)
 - [Article](docs/Model/Article.md)
 - [ArticleStub](docs/Model/ArticleStub.md)
 - [ArticleType](docs/Model/ArticleType.md)
 - [ArticleTypeDetails](docs/Model/ArticleTypeDetails.md)
 - [Author](docs/Model/Author.md)
 - [Block](docs/Model/Block.md)
 - [BoxInfo](docs/Model/BoxInfo.md)
 - [BoxType](docs/Model/BoxType.md)
 - [Category](docs/Model/Category.md)
 - [Cutoff](docs/Model/Cutoff.md)
 - [ImageInfo](docs/Model/ImageInfo.md)
 - [Paper](docs/Model/Paper.md)
 - [Scoring](docs/Model/Scoring.md)


## Documentation For Authorization

All endpoints do not require authorization.

## Author



