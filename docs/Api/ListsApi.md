# OpenAPI\Client\ListsApi

All URIs are relative to *http://http:/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**frontpageGet**](ListsApi.md#frontpageGet) | **GET** /frontpage | Returns a list for a front page
[**latestGet**](ListsApi.md#latestGet) | **GET** /latest | Returns a list of latest articles
[**mostreadGet**](ListsApi.md#mostreadGet) | **GET** /mostread | Returns a list of most read articles
[**searchGet**](ListsApi.md#searchGet) | **GET** /search | Returns a list of search results



## frontpageGet

> \OpenAPI\Client\Model\ArticleStub[] frontpageGet($start, $limit, $category, $paper)

Returns a list for a front page

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$start = 56; // int | 
$limit = 56; // int | 
$category = 'category_example'; // string | 
$paper = 'paper_example'; // string | 

try {
    $result = $apiInstance->frontpageGet($start, $limit, $category, $paper);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->frontpageGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start** | **int**|  | [optional]
 **limit** | **int**|  | [optional]
 **category** | **string**|  | [optional]
 **paper** | **string**|  | [optional]

### Return type

[**\OpenAPI\Client\Model\ArticleStub[]**](../Model/ArticleStub.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## latestGet

> \OpenAPI\Client\Model\ArticleStub[] latestGet($start, $limit, $paper)

Returns a list of latest articles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$start = 56; // int | 
$limit = 56; // int | 
$paper = 'paper_example'; // string | 

try {
    $result = $apiInstance->latestGet($start, $limit, $paper);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->latestGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start** | **int**|  | [optional]
 **limit** | **int**|  | [optional]
 **paper** | **string**|  | [optional]

### Return type

[**\OpenAPI\Client\Model\ArticleStub[]**](../Model/ArticleStub.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## mostreadGet

> \OpenAPI\Client\Model\ArticleStub[] mostreadGet($start, $limit, $category, $paper, $only_subscribers)

Returns a list of most read articles

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$start = 56; // int | 
$limit = 56; // int | 
$category = 'category_example'; // string | 
$paper = 'paper_example'; // string | 
$only_subscribers = True; // bool | 

try {
    $result = $apiInstance->mostreadGet($start, $limit, $category, $paper, $only_subscribers);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->mostreadGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **start** | **int**|  | [optional]
 **limit** | **int**|  | [optional]
 **category** | **string**|  | [optional]
 **paper** | **string**|  | [optional]
 **only_subscribers** | **bool**|  | [optional]

### Return type

[**\OpenAPI\Client\Model\ArticleStub[]**](../Model/ArticleStub.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## searchGet

> \OpenAPI\Client\Model\ArticleStub[] searchGet($start, $limit, $paper, $content_query)

Returns a list of search results

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$start = 56; // int | 
$limit = 56; // int | 
$paper = 'paper_example'; // string | 
$content_query = 'content_query_example'; // string | 

try {
    $result = $apiInstance->searchGet($start, $limit, $paper, $content_query);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->searchGet: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ArticleStub[]**](../Model/ArticleStub.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

