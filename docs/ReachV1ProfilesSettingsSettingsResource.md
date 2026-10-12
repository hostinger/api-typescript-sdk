# ReachV1ProfilesSettingsSettingsResource

Sender identity and brand details saved on the profile.  A profile that never filled its settings in returns empty values, so every field can be `null`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brand_name** | **string** |  | [optional] [default to undefined]
**website_url** | **string** |  | [optional] [default to undefined]
**business_address** | **string** |  | [optional] [default to undefined]
**privacy_policy_url** | **string** |  | [optional] [default to undefined]
**accent_color** | **string** |  | [optional] [default to undefined]
**button_color** | **string** |  | [optional] [default to undefined]
**background_color** | **string** |  | [optional] [default to undefined]
**text_color** | **string** |  | [optional] [default to undefined]
**links_color** | **string** |  | [optional] [default to undefined]
**button_text** | **string** | Button text colour. | [optional] [default to undefined]
**button_corners** | **number** | Button corner radius in pixels. | [optional] [default to undefined]
**font_family** | **string** | Body and button font. | [optional] [default to undefined]
**heading_font_family** | **string** |  | [optional] [default to undefined]
**logo_url** | **string** |  | [optional] [default to undefined]
**social_links** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**socials** | **{ [key: string]: string; }** | Social profile links keyed by platform. | [optional] [default to undefined]
**about** | **string** |  | [optional] [default to undefined]
**keywords** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**topics** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**selling_points** | **Array&lt;string&gt;** |  | [optional] [default to undefined]
**sender_name** | **string** | Default sender name that campaigns created afterwards start from. | [optional] [default to undefined]
**sender_email** | **string** | Part of the default sender address before the &#x60;@&#x60;. It is combined with the profile\&#39;s connected sending domain, see the connected sending domain endpoint. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ProfilesSettingsSettingsResource } from '@hostinger/sdk';

const instance: ReachV1ProfilesSettingsSettingsResource = {
    brand_name,
    website_url,
    business_address,
    privacy_policy_url,
    accent_color,
    button_color,
    background_color,
    text_color,
    links_color,
    button_text,
    button_corners,
    font_family,
    heading_font_family,
    logo_url,
    social_links,
    socials,
    about,
    keywords,
    topics,
    selling_points,
    sender_name,
    sender_email,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
