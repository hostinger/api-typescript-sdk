# WordPressV1LoginLoginLinksResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**login** | **string** | Primary auto-login URL for the WordPress installation | [optional] [default to undefined]
**fallback** | **string** | Fallback auto-login URL using the temporary Hostinger domain | [optional] [default to undefined]
**_default** | **string** | Default WordPress admin URL used when auto-login is unavailable | [optional] [default to undefined]

## Example

```typescript
import { WordPressV1LoginLoginLinksResource } from 'hostinger-api-sdk';

const instance: WordPressV1LoginLoginLinksResource = {
    login,
    fallback,
    _default,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
