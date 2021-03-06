# Numary\Ledger\StatsApi

All URIs are relative to https://.o.numary.cloud/ledger.

Method | HTTP request | Description
------------- | ------------- | -------------
[**readStats()**](StatsApi.md#readStats) | **GET** /{ledger}/stats | Get Stats


## `readStats()`

```php
readStats($ledger): \Numary\Ledger\Model\StatsResponse
```

Get Stats

Get ledger stats (aggregate metrics on accounts and transactions) The stats for account

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = Numary\Ledger\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Numary\Ledger\Api\StatsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ledger = ledger001; // string | name of the ledger

try {
    $result = $apiInstance->readStats($ledger);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StatsApi->readStats: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ledger** | **string**| name of the ledger |

### Return type

[**\Numary\Ledger\Model\StatsResponse**](../Model/StatsResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
