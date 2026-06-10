# HostingV1DatabasesCreateDatabaseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Database name. If the account username prefix is omitted, it is added automatically. | [default to undefined]
**user** | **string** | Database user. If the account username prefix is omitted, it is added automatically. | [default to undefined]
**password** | **string** | Database user password. | [default to undefined]
**website_domain** | **string** | Website domain assigned to the database. | [default to undefined]

## Example

```typescript
import { HostingV1DatabasesCreateDatabaseRequest } from 'hostinger-api-sdk';

const instance: HostingV1DatabasesCreateDatabaseRequest = {
    name,
    user,
    password,
    website_domain,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
