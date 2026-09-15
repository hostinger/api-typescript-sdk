# HostingV1GitGitInstallationResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** | Installation identifier. Use it as the path parameter of List Git installation repositories. | [default to undefined]
**provider** | **string** | Git provider the account belongs to | [default to undefined]
**account_login** | **string** | Login of the connected provider account (user or organization) | [default to undefined]
**account_type** | **string** | Whether the connected account is a user or an organization | [default to undefined]
**account_avatar_url** | **string** | Avatar URL of the connected provider account | [default to undefined]
**status** | **string** | Installation status. Only active installations are listed unless the status filter says otherwise. | [default to undefined]
**installed_at** | **string** | When the provider app was installed on the account | [default to undefined]
**created_at** | **string** | When the installation record was created | [default to undefined]
**has_oauth** | **boolean** | True when the GitHub user account has a stored OAuth token whose refresh token is still valid, false when the token is missing or its refresh token expired. Null for organization accounts and for providers other than GitHub. | [default to undefined]

## Example

```typescript
import { HostingV1GitGitInstallationResource } from '@hostinger/sdk';

const instance: HostingV1GitGitInstallationResource = {
    uuid,
    provider,
    account_login,
    account_type,
    account_avatar_url,
    status,
    installed_at,
    created_at,
    has_oauth,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
