# WordPressV1InstallationsWordPressMcpDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **string** | JWT used to authenticate against the installation MCP server | [optional] [default to undefined]
**mcp_url** | **string** | MCP (Model Context Protocol) endpoint URL for the WordPress installation | [optional] [default to undefined]
**expires_in** | **number** | Token lifetime in seconds from the moment it was issued | [optional] [default to undefined]
**expires_at** | **string** | Date-time at which the token expires | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1InstallationsWordPressMcpDetailsResource } from 'hostinger-api-sdk';

const instance: WordPressV1InstallationsWordPressMcpDetailsResource = {
    token,
    mcp_url,
    expires_in,
    expires_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
