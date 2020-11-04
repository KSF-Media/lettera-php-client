# OpenAPI\Client\ArticlesApi

All URIs are relative to *http://http:/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**articleUuidGet**](ArticlesApi.md#articleUuidGet) | **GET** /article/{uuid} | 
[**articleUuidStubGet**](ArticlesApi.md#articleUuidStubGet) | **GET** /article/{uuid}/stub | 



## articleUuidGet

> \OpenAPI\Client\Model\Article articleUuidGet($uuid, $auth_user, $authorization, $textonly)



Fetch article by UUID.   Notes about the images:   The image URLs point to our image scaler, and are returned without scaling parameters.  However, if wanted, `width` and `height` parameters can be added to the querystring of the URL.  Also in list views, to ensure same size, it might be useful to crop the images by using the parameter `function=hardcrop`

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


## articleUuidStubGet

> \OpenAPI\Client\Model\ArticleStub articleUuidStubGet($uuid, $auth_user, $authorization)



Fetch an article stub by UUID

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

try {
    $result = $apiInstance->articleUuidStubGet($uuid, $auth_user, $authorization);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ArticlesApi->articleUuidStubGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uuid** | [**string**](../Model/.md)|  |
 **auth_user** | [**string**](../Model/.md)|  | [optional]
 **authorization** | **string**|  | [optional]

### Return type

[**\OpenAPI\Client\Model\ArticleStub**](../Model/ArticleStub.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

