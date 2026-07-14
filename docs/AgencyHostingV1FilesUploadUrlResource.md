# AgencyHostingV1FilesUploadUrlResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **string** | The TUS upload endpoint URL to send upload requests to | [default to undefined]
**auth_key** | **string** | Authentication token to pass as the &#x60;X-Auth&#x60; header in TUS upload requests | [default to undefined]
**rest_auth_key** | **string** | Authentication token to pass as the &#x60;X-Auth-Rest&#x60; header in TUS upload requests | [default to undefined]

## Example

```typescript
import { AgencyHostingV1FilesUploadUrlResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1FilesUploadUrlResource = {
    url,
    auth_key,
    rest_auth_key,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
