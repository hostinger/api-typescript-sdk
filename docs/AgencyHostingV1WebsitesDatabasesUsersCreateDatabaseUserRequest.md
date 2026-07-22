# AgencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**database_user** | **string** | Database username to create (alphanumeric and underscores). | [default to undefined]
**password** | **string** | Password for the database user (requires mixed case, letters, and numbers). | [default to undefined]
**host** | **string** | Host the user connects from (IPv4, IPv6, % wildcard, or localhost). Defaults to localhost. | [optional] [default to undefined]

## Example

```typescript
import { AgencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest } from 'hostinger-api-sdk';

const instance: AgencyHostingV1WebsitesDatabasesUsersCreateDatabaseUserRequest = {
    database_user,
    password,
    host,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
