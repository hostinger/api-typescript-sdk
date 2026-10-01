# WordPressV1McpExecuteMcpToolRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tool_name** | **string** | Tool name as returned by the List MCP tools endpoint. | [default to undefined]
**parameters** | **{ [key: string]: any; }** | Tool input matching the input schema returned by the Show MCP tool info endpoint. | [optional] [default to undefined]
**server** | **string** | MCP server exposing the tool. Defaults to the mcp-adapter default server. | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1McpExecuteMcpToolRequest } from '@hostinger/sdk';

const instance: WordPressV1McpExecuteMcpToolRequest = {
    tool_name,
    parameters,
    server,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
