# HlsApiClient::ConvertRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_token** | **String** | API token |  |
| **job_id** | **String** | Job ID; identifier; unique; alpha and dash only, min 4, max 50 chars |  |
| **input_source_url** | **String** | URL to download input media from |  |
| **file_type** | **String** | The media type of the inputSourceUrl |  |
| **callback** | **String** | An URL to which Job will POST status updates |  |

## Example

```ruby
require 'hls_api_client'

instance = HlsApiClient::ConvertRequest.new(
  api_token: null,
  job_id: null,
  input_source_url: null,
  file_type: null,
  callback: null
)
```

