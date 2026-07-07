# WordPressV1InstallationsJwtTokenResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **string** | Signed JWT used to authenticate requests against the WordPress installation | [optional] [default to undefined]
**expires_in** | **number** | Token lifetime in seconds from the moment it was issued | [optional] [default to undefined]
**expires_at** | **string** | Date-time at which the token expires, or null when not provided | [optional] [default to undefined]
**mcp_url** | **string** | MCP (Model Context Protocol) endpoint URL for the WordPress installation, or null when not provided | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1InstallationsJwtTokenResource } from 'hostinger-api-sdk';

const instance: WordPressV1InstallationsJwtTokenResource = {
    token,
    expires_in,
    expires_at,
    mcp_url,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
