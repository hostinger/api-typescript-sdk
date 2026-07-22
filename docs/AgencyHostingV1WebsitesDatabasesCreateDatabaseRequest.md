# AgencyHostingV1WebsitesDatabasesCreateDatabaseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**database_name** | **string** | Database name to create (alphanumeric characters). | [default to undefined]
**database_user** | **string** | Database username to create alongside the database (alphanumeric characters). | [default to undefined]
**password** | **string** | Password for the database user (requires mixed case, letters, and numbers). | [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesDatabasesCreateDatabaseRequest } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesDatabasesCreateDatabaseRequest = {
    database_name,
    database_user,
    password,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
