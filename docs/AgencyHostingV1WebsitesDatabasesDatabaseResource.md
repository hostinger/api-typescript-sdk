# AgencyHostingV1WebsitesDatabasesDatabaseResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Database name. | [optional] [default to undefined]
**created_at** | **string** | Database creation date in ISO 8601 format. | [optional] [default to undefined]
**users** | [**Array&lt;AgencyHostingV1WebsitesDatabasesDatabaseUserResource&gt;**](AgencyHostingV1WebsitesDatabasesDatabaseUserResource.md) | Non-system users that can access the database. | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesDatabasesDatabaseResource } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesDatabasesDatabaseResource = {
    name,
    created_at,
    users,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
