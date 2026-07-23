# MailV1ApiTokensApiTokenResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique API token identifier | [optional] [default to undefined]
**order_id** | **string** | Resource ID of the owning mail order | [optional] [default to undefined]
**name** | **string** | Human-readable label for this token | [optional] [default to undefined]
**scope** | [**MailV1ApiTokensApiTokenScopeResource**](MailV1ApiTokensApiTokenScopeResource.md) |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**last_used_at** | **string** | Last successful authentication using this token | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { MailV1ApiTokensApiTokenResource } from 'hostinger-api-sdk';

const instance: MailV1ApiTokensApiTokenResource = {
    id,
    order_id,
    name,
    scope,
    created_at,
    last_used_at,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
