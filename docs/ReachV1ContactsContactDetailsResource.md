# ReachV1ContactsContactDetailsResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **string** |  | [optional] [default to undefined]
**email** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**surname** | **string** |  | [optional] [default to undefined]
**phone** | **string** |  | [optional] [default to undefined]
**subscription_status** | **string** |  | [optional] [default to undefined]
**subscribed_at** | **string** |  | [optional] [default to undefined]
**unsubscribed_at** | **string** |  | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]
**domain** | **string** |  | [optional] [default to undefined]
**source** | **string** |  | [optional] [default to undefined]
**note** | **string** |  | [optional] [default to undefined]
**tags** | [**Array&lt;ReachV1ContactsTagsTagResource&gt;**](ReachV1ContactsTagsTagResource.md) |  | [optional] [default to undefined]
**fields** | [**Array&lt;ReachV1ContactsFieldsContactFieldValueResource&gt;**](ReachV1ContactsFieldsContactFieldValueResource.md) | Custom field values held by this contact | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsContactDetailsResource } from 'hostinger-api-sdk';

const instance: ReachV1ContactsContactDetailsResource = {
    uuid,
    email,
    name,
    surname,
    phone,
    subscription_status,
    subscribed_at,
    unsubscribed_at,
    created_at,
    domain,
    source,
    note,
    tags,
    fields,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
