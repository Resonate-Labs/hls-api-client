# HlsApiClient::ConversionControllerApi

All URIs are relative to *https://hls.cloud.beta.weresonate.com*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**callback_echo**](ConversionControllerApi.md#callback_echo) | **POST** /api/v2/callbackEcho | Do-nothing, replies with the input; this exists just facilitate using the CallbackConvert datatype to receive callbacks |
| [**convert**](ConversionControllerApi.md#convert) | **POST** /api/v2/convert | Start a conversion job |
| [**delete_job_results**](ConversionControllerApi.md#delete_job_results) | **DELETE** /api/v2/delete | Delete artifacts from a given job |


## callback_echo

> <ConvertCallback> callback_echo(convert_callback)

Do-nothing, replies with the input; this exists just facilitate using the CallbackConvert datatype to receive callbacks

### Examples

```ruby
require 'time'
require 'hls_api_client'

api_instance = HlsApiClient::ConversionControllerApi.new
convert_callback = HlsApiClient::ConvertCallback.new({job_id: 'job_id_example', result: 'CREATING', version: 'version_example'}) # ConvertCallback | 

begin
  # Do-nothing, replies with the input; this exists just facilitate using the CallbackConvert datatype to receive callbacks
  result = api_instance.callback_echo(convert_callback)
  p result
rescue HlsApiClient::ApiError => e
  puts "Error when calling ConversionControllerApi->callback_echo: #{e}"
end
```

#### Using the callback_echo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ConvertCallback>, Integer, Hash)> callback_echo_with_http_info(convert_callback)

```ruby
begin
  # Do-nothing, replies with the input; this exists just facilitate using the CallbackConvert datatype to receive callbacks
  data, status_code, headers = api_instance.callback_echo_with_http_info(convert_callback)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ConvertCallback>
rescue HlsApiClient::ApiError => e
  puts "Error when calling ConversionControllerApi->callback_echo_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **convert_callback** | [**ConvertCallback**](ConvertCallback.md) |  |  |

### Return type

[**ConvertCallback**](ConvertCallback.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: */*


## convert

> convert(convert_request)

Start a conversion job

### Examples

```ruby
require 'time'
require 'hls_api_client'

api_instance = HlsApiClient::ConversionControllerApi.new
convert_request = HlsApiClient::ConvertRequest.new({api_token: 'api_token_example', job_id: 'job_id_example', input_source_url: 'input_source_url_example', file_type: 'file_type_example', callback: 'callback_example'}) # ConvertRequest | 

begin
  # Start a conversion job
  api_instance.convert(convert_request)
rescue HlsApiClient::ApiError => e
  puts "Error when calling ConversionControllerApi->convert: #{e}"
end
```

#### Using the convert_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> convert_with_http_info(convert_request)

```ruby
begin
  # Start a conversion job
  data, status_code, headers = api_instance.convert_with_http_info(convert_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue HlsApiClient::ApiError => e
  puts "Error when calling ConversionControllerApi->convert_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **convert_request** | [**ConvertRequest**](ConvertRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined


## delete_job_results

> delete_job_results(delete_request)

Delete artifacts from a given job

### Examples

```ruby
require 'time'
require 'hls_api_client'

api_instance = HlsApiClient::ConversionControllerApi.new
delete_request = HlsApiClient::DeleteRequest.new({api_token: 'api_token_example', job_id: 'job_id_example'}) # DeleteRequest | 

begin
  # Delete artifacts from a given job
  api_instance.delete_job_results(delete_request)
rescue HlsApiClient::ApiError => e
  puts "Error when calling ConversionControllerApi->delete_job_results: #{e}"
end
```

#### Using the delete_job_results_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_job_results_with_http_info(delete_request)

```ruby
begin
  # Delete artifacts from a given job
  data, status_code, headers = api_instance.delete_job_results_with_http_info(delete_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue HlsApiClient::ApiError => e
  puts "Error when calling ConversionControllerApi->delete_job_results_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delete_request** | [**DeleteRequest**](DeleteRequest.md) |  |  |

### Return type

nil (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

