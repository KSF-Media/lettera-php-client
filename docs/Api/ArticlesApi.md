# OpenAPI\Client\ArticlesApi

All URIs are relative to *http://http:/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**articleSearchGet**](ArticlesApi.md#articleSearchGet) | **GET** /article/search | 
[**articleUuidGet**](ArticlesApi.md#articleUuidGet) | **GET** /article/{uuid} | 



## articleSearchGet

> \OpenAPI\Client\Model\Article[] articleSearchGet($start, $limit, $paper, $content_query)



Search article by content. It's a freetext search, so the `contentQuery` may be whatever string or sentence to search for.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ArticlesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$start = 56; // int | 
$limit = 56; // int | 
$paper = 'paper_example'; // string | 
$content_query = 'content_query_example'; // string | 

try {
    $result = $apiInstance->articleSearchGet($start, $limit, $paper, $content_query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articleSearchGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start** | **int**|  | [optional]
 **limit** | **int**|  | [optional]
 **paper** | **string**|  | [optional]
 **content_query** | **string**|  | [optional]

### Return type

[**\OpenAPI\Client\Model\Article[]**](../Model/Article.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## articleUuidGet

> \OpenAPI\Client\Model\Article articleUuidGet($uuid, $auth_user, $authorization, $textonly)



Fetch article by UUID.   Notes about the images:   The image URLs point to our image scaler, and are returned without no scaling parameters.  However, if wanted, `width` and `height` parameters can be added to the querystring of the URL.  Also in list views, to ensure same size, it might be useful to crop the images by using the parameter `function=hardcrop`

### Example

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
$textonly = false; // bool | 

try {
    $result = $apiInstance->articleUuidGet($uuid, $auth_user, $authorization, $textonly);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articleUuidGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**string**](../Model/.md)|  |
 **auth_user** | [**string**](../Model/.md)|  | [optional]
 **authorization** | **string**|  | [optional]
 **textonly** | **bool**|  | [optional] [default to false]

### Return type

[**\OpenAPI\Client\Model\Article**](../Model/Article.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

