# WordPressV1ThemesThemeResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **string** | Theme slug used when installing the theme | [optional] [default to undefined]
**title** | **string** | Human readable theme name | [optional] [default to undefined]
**url** | **string** | Link to the theme page on WordPress.org | [optional] [default to undefined]
**featured_image_url** | **string** | URL of the theme preview thumbnail | [optional] [default to undefined]
**full_image_url** | **string** | URL of the full-size theme preview image | [optional] [default to undefined]
**description** | **string** | Short theme description | [optional] [default to undefined]
**logo_url** | **string** | URL of the theme logo | [optional] [default to undefined]
**is_plan_upgrade_needed** | **boolean** | Whether a hosting plan upgrade is required to use the theme | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1ThemesThemeResource } from 'hostinger-api-sdk';

const instance: WordPressV1ThemesThemeResource = {
    slug,
    title,
    url,
    featured_image_url,
    full_image_url,
    description,
    logo_url,
    is_plan_upgrade_needed,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
