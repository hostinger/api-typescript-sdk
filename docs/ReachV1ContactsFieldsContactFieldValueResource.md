# ReachV1ContactsFieldsContactFieldValueResource

A custom contact field together with the value held by one contact

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**type** | **string** |  | [optional] [default to undefined]
**label** | **string** |  | [optional] [default to undefined]
**slug** | **string** |  | [optional] [default to undefined]
**value** | **string** | Set for the scalar field types, null for the choice types | [optional] [default to undefined]
**selected_option_uuids** | **Array&lt;string&gt;** | Chosen options for the choice field types, empty for the scalar types | [optional] [default to undefined]
**_options** | [**Array&lt;ReachV1ContactsFieldsContactFieldOptionResource&gt;**](ReachV1ContactsFieldsContactFieldOptionResource.md) | Every option the field offers, not only the selected ones | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsFieldsContactFieldValueResource } from '@hostinger/sdk';

const instance: ReachV1ContactsFieldsContactFieldValueResource = {
    uuid,
    type,
    label,
    slug,
    value,
    selected_option_uuids,
    _options,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
