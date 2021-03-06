# Numary\Ledger\ServerApi

All URIs are relative to https://.o.numary.cloud/ledger.

Method | HTTP request | Description
------------- | ------------- | -------------
[**getInfo()**](ServerApi.md#getInfo) | **GET** /_info | Show server information.


## `getInfo()`

```php
getInfo(): \Numary\Ledger\Model\ConfigInfoResponse
```

Show server information.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = Numary\Ledger\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new Numary\Ledger\Api\ServerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getInfo();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServerApi->getInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\Numary\Ledger\Model\ConfigInfoResponse**](../Model/ConfigInfoResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
