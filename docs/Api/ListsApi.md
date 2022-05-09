# OpenAPI\Client\ListsApi

All URIs are relative to *http://http:/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**frontpageGet**](ListsApi.md#frontpageGet) | **GET** /frontpage | Returns a list for a front page
[**latestGet**](ListsApi.md#latestGet) | **GET** /latest | Returns a list of latest articles
[**mostreadGet**](ListsApi.md#mostreadGet) | **GET** /mostread | Returns a list of most read articles
[**presetPresetCategoryGet**](ListsApi.md#presetPresetCategoryGet) | **GET** /preset/{preset}/{category} | Load a preset model
[**presetPresetCategoryPost**](ListsApi.md#presetPresetCategoryPost) | **POST** /preset/{preset}/{category} | Update a preset model
[**scoredPost**](ListsApi.md#scoredPost) | **POST** /scored | List recent articles sorted by given scoring weights
[**scoredPresetGet**](ListsApi.md#scoredPresetGet) | **GET** /scored/{preset} | List recent articles sorted by preset scoring
[**searchGet**](ListsApi.md#searchGet) | **GET** /search | Returns a list of search results
[**tagTagGet**](ListsApi.md#tagTagGet) | **GET** /tag/{tag} | Returns a list of latest articles by tag



## frontpageGet

> object frontpageGet($start, $limit, $category, $paper)

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

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8, application/rss+xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## latestGet

> object latestGet($start, $limit, $paper)

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

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8, application/rss+xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## mostreadGet

> object mostreadGet($start, $limit, $category, $paper, $only_subscribers)

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

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## presetPresetCategoryGet

> \OpenAPI\Client\Model\Scoring presetPresetCategoryGet($auth_user, $authorization, $preset, $category)

Load a preset model

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_user = 'auth_user_example'; // string | 
$authorization = 'authorization_example'; // string | 
$preset = 56; // int | 
$category = 'category_example'; // string | 

try {
    $result = $apiInstance->presetPresetCategoryGet($auth_user, $authorization, $preset, $category);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->presetPresetCategoryGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_user** | [**string**](../Model/.md)|  |
 **authorization** | **string**|  |
 **preset** | **int**|  |
 **category** | **string**|  |

### Return type

[**\OpenAPI\Client\Model\Scoring**](../Model/Scoring.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## presetPresetCategoryPost

> presetPresetCategoryPost($auth_user, $authorization, $preset, $category, $body)

Update a preset model

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$auth_user = 'auth_user_example'; // string | 
$authorization = 'authorization_example'; // string | 
$preset = 56; // int | 
$category = 'category_example'; // string | 
$body = new \OpenAPI\Client\Model\Scoring(); // \OpenAPI\Client\Model\Scoring | 

try {
    $apiInstance->presetPresetCategoryPost($auth_user, $authorization, $preset, $category, $body);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->presetPresetCategoryPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_user** | [**string**](../Model/.md)|  |
 **authorization** | **string**|  |
 **preset** | **int**|  |
 **category** | **string**|  |
 **body** | [**\OpenAPI\Client\Model\Scoring**](../Model/Scoring.md)|  |

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json;charset=utf-8
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## scoredPost

> \OpenAPI\Client\Model\ArticleStub[] scoredPost($category, $paper, $body, $start, $limit)

List recent articles sorted by given scoring weights

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$category = 'category_example'; // string | 
$paper = 'paper_example'; // string | 
$body = new \OpenAPI\Client\Model\Scoring(); // \OpenAPI\Client\Model\Scoring | 
$start = 56; // int | 
$limit = 56; // int | 

try {
    $result = $apiInstance->scoredPost($category, $paper, $body, $start, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->scoredPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category** | **string**|  |
 **paper** | **string**|  |
 **body** | [**\OpenAPI\Client\Model\Scoring**](../Model/Scoring.md)|  |
 **start** | **int**|  | [optional]
 **limit** | **int**|  | [optional]

### Return type

[**\OpenAPI\Client\Model\ArticleStub[]**](../Model/ArticleStub.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json;charset=utf-8
- **Accept**: application/json;charset=utf-8

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)


## scoredPresetGet

> \OpenAPI\Client\Model\ArticleStub[] scoredPresetGet($preset, $category, $start, $limit, $paper)

List recent articles sorted by preset scoring

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$preset = 56; // int | 
$category = 'category_example'; // string | 
$start = 56; // int | 
$limit = 56; // int | 
$paper = 'paper_example'; // string | 

try {
    $result = $apiInstance->scoredPresetGet($preset, $category, $start, $limit, $paper);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->scoredPresetGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **preset** | **int**|  |
 **category** | **string**|  |
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


## tagTagGet

> object tagTagGet($tag, $start, $limit, $paper)

Returns a list of latest articles by tag

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


$apiInstance = new OpenAPI\Client\Api\ListsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$tag = 'tag_example'; // string | 
$start = 56; // int | 
$limit = 56; // int | 
$paper = 'paper_example'; // string | 

try {
    $result = $apiInstance->tagTagGet($tag, $start, $limit, $paper);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListsApi->tagTagGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tag** | **string**|  |
 **start** | **int**|  | [optional]
 **limit** | **int**|  | [optional]
 **paper** | **string**|  | [optional]

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json;charset=utf-8, application/rss+xml

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../../README.md#documentation-for-models)
[[Back to README]](../../README.md)

