# OpenAPI\Client\DefaultApi

All URIs are relative to https://api.adres-validatie.nl, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**accessTokenPost()**](DefaultApi.md#accessTokenPost) | **POST** /access-token |  |
| [**accountPost()**](DefaultApi.md#accountPost) | **POST** /account |  |
| [**accountWebhookPut()**](DefaultApi.md#accountWebhookPut) | **PUT** /account/webhook |  |
| [**fileAddressesCsvGet()**](DefaultApi.md#fileAddressesCsvGet) | **GET** /file/addresses.csv |  |
| [**fileAddressesZipGet()**](DefaultApi.md#fileAddressesZipGet) | **GET** /file/addresses.zip |  |
| [**stripeCheckoutSessionPost()**](DefaultApi.md#stripeCheckoutSessionPost) | **POST** /stripe/checkout/session |  |
| [**stripePortalSessionPost()**](DefaultApi.md#stripePortalSessionPost) | **POST** /stripe/portal/session |  |


## `accessTokenPost()`

```php
accessTokenPost($client_id, $client_secret): \OpenAPI\Client\Model\AccessTokenPost200Response
```



Creates a short-lived bearer token for API consumers

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$client_id = 'client_id_example'; // string | The account's client id
$client_secret = 'client_secret_example'; // string | The account's client secret

try {
    $result = $apiInstance->accessTokenPost($client_id, $client_secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->accessTokenPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **client_id** | **string**| The account&#39;s client id | |
| **client_secret** | **string**| The account&#39;s client secret | |

### Return type

[**\OpenAPI\Client\Model\AccessTokenPost200Response**](../Model/AccessTokenPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountPost()`

```php
accountPost($email, $webhook): \OpenAPI\Client\Model\AccountPost200Response
```



Sign up endpoint for new users (does not require authorization)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$email = 'email_example'; // string | The user's email
$webhook = 'webhook_example'; // string | The url webhook messages will be sent to

try {
    $result = $apiInstance->accountPost($email, $webhook);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->accountPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email** | **string**| The user&#39;s email | |
| **webhook** | **string**| The url webhook messages will be sent to | |

### Return type

[**\OpenAPI\Client\Model\AccountPost200Response**](../Model/AccountPost200Response.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `accountWebhookPut()`

```php
accountWebhookPut($webhook): \OpenAPI\Client\Model\AccountWebhookPut200Response
```



Endpoint for updating webhook url

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$webhook = 'webhook_example'; // string | The url webhook messages will be sent to

try {
    $result = $apiInstance->accountWebhookPut($webhook);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->accountWebhookPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **webhook** | **string**| The url webhook messages will be sent to | |

### Return type

[**\OpenAPI\Client\Model\AccountWebhookPut200Response**](../Model/AccountWebhookPut200Response.md)

### Authorization

[Oauth2](../../README.md#Oauth2)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `fileAddressesCsvGet()`

```php
fileAddressesCsvGet(): \OpenAPI\Client\Model\FileAddressesCsvGet200Response
```



Endpoint retrieving a download url for the latest addresses.csv, only use this if you can not extract zip files!

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->fileAddressesCsvGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->fileAddressesCsvGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\FileAddressesCsvGet200Response**](../Model/FileAddressesCsvGet200Response.md)

### Authorization

[Oauth2](../../README.md#Oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `fileAddressesZipGet()`

```php
fileAddressesZipGet(): \OpenAPI\Client\Model\FileAddressesZipGet200Response
```



Endpoint retrieving a download url for the latest addresses.zip

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->fileAddressesZipGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->fileAddressesZipGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\FileAddressesZipGet200Response**](../Model/FileAddressesZipGet200Response.md)

### Authorization

[Oauth2](../../README.md#Oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `stripeCheckoutSessionPost()`

```php
stripeCheckoutSessionPost($success_url, $cancel_url): \OpenAPI\Client\Model\StripeCheckoutSessionPost200Response
```



Endpoint for retrieving a Stripe checkout session url

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$success_url = 'success_url_example'; // string | The url the user-client will be redirected to after successful payment
$cancel_url = 'cancel_url_example'; // string | The url the user-client will be redirected to after payment is cancelled

try {
    $result = $apiInstance->stripeCheckoutSessionPost($success_url, $cancel_url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->stripeCheckoutSessionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **success_url** | **string**| The url the user-client will be redirected to after successful payment | |
| **cancel_url** | **string**| The url the user-client will be redirected to after payment is cancelled | |

### Return type

[**\OpenAPI\Client\Model\StripeCheckoutSessionPost200Response**](../Model/StripeCheckoutSessionPost200Response.md)

### Authorization

[Oauth2](../../README.md#Oauth2)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `stripePortalSessionPost()`

```php
stripePortalSessionPost($return_url): \OpenAPI\Client\Model\StripePortalSessionPost200Response
```



Endpoint for retrieving a Stripe portal session url

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DefaultApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$return_url = 'return_url_example'; // string | The url the user-client will be redirected to when leaving the portal

try {
    $result = $apiInstance->stripePortalSessionPost($return_url);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DefaultApi->stripePortalSessionPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **return_url** | **string**| The url the user-client will be redirected to when leaving the portal | |

### Return type

[**\OpenAPI\Client\Model\StripePortalSessionPost200Response**](../Model/StripePortalSessionPost200Response.md)

### Authorization

[Oauth2](../../README.md#Oauth2)

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
