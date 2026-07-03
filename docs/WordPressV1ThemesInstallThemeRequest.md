# WordPressV1ThemesInstallThemeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**theme** | **string** | Slug of the theme to install. Hostinger theme slugs (hostinger-blog, hostinger-affiliate-theme, hostinger-ai-theme) trigger the custom installer and forward the optional palette/layout/font fields; any other WordPress theme slug uses the standard installer and ignores those fields. | [default to undefined]
**palette** | **string** | Palette identifier. Only applied when the theme is a Hostinger theme; the default is used when omitted. | [optional] [default to 'palette1']
**layout** | **string** | Layout identifier. Only applied when the theme is a Hostinger theme; the default is used when omitted. | [optional] [default to 'layout1']
**font** | **string** | Font identifier. Only applied when the theme is a Hostinger theme; the default is used when omitted. | [optional] [default to FontEnum_Default]

## Example

```typescript
import { WordPressV1ThemesInstallThemeRequest } from 'hostinger-api-sdk';

const instance: WordPressV1ThemesInstallThemeRequest = {
    theme,
    palette,
    layout,
    font,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
