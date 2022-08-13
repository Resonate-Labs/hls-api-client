# HlsApiClient::ConvertCallback

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** | Original Job ID of the conversion |  |
| **result** | **String** | Current status of the conversion |  |
| **version** | **String** | Version of the Conversion Service |  |
| **encoding_profile** | **String** | Version of the encoding profile used | [optional] |

## Example

```ruby
require 'hls_api_client'

instance = HlsApiClient::ConvertCallback.new(
  job_id: null,
  result: null,
  version: null,
  encoding_profile: null
)
```

