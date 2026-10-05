# WordPressV1InstallationsInstallWordPressRequestDatabase

Optional. If the named database already exists on the account, it is used for this WordPress install. Otherwise a new database is created with this name, or with a generated name when database is omitted or null. A new database gets a random database user and counts toward the plan\'s database limit.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Database name (username prefix added if missing) | [optional] [default to undefined]
**password** | **string** | Password for a new database. Random when omitted or null. Ignored when the named database already exists. | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1InstallationsInstallWordPressRequestDatabase } from '@hostinger/sdk';

const instance: WordPressV1InstallationsInstallWordPressRequestDatabase = {
    name,
    password,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
