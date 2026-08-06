# ReachV1ContactsUpdateRequest

Fields to change on a contact. Omitted properties are left untouched.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** |  | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**surname** | **string** |  | [optional] [default to undefined]
**phone** | **string** | Phone number in E.164 format (leading \&quot;+\&quot; then 7-15 digits) | [optional] [default to undefined]
**subscription_status** | **string** |  | [optional] [default to undefined]
**note** | **string** |  | [optional] [default to undefined]
**fields** | [**Array&lt;ReachV1ContactsUpdateRequestFieldsInner&gt;**](ReachV1ContactsUpdateRequestFieldsInner.md) | Set custom field values. Omit to leave untouched, send an empty array to clear them all. | [optional] [default to undefined]

## Example

```typescript
import { ReachV1ContactsUpdateRequest } from 'hostinger-api-sdk';

const instance: ReachV1ContactsUpdateRequest = {
    email,
    name,
    surname,
    phone,
    subscription_status,
    note,
    fields,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
