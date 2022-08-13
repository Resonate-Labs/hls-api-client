# HlsApiClient::DeleteRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_token** | **String** | API token |  |
| **job_id** | **String** | Job ID; identifier; unique; alpha and dash only, min 4, max 50 chars |  |

## Example

```ruby
require 'hls_api_client'

instance = HlsApiClient::DeleteRequest.new(
  api_token: null,
  job_id: null
)
```

