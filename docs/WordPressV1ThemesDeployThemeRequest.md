# WordPressV1ThemesDeployThemeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **string** | Slug of the theme | [default to undefined]
**theme_path** | **string** | Relative path to the theme directory from wp-content/themes | [default to undefined]
**is_activated** | **boolean** | Whether to activate the theme after deployment | [optional] [default to false]

## Example

```typescript
import { WordPressV1ThemesDeployThemeRequest } from 'hostinger-api-sdk';

const instance: WordPressV1ThemesDeployThemeRequest = {
    slug,
    theme_path,
    is_activated,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
