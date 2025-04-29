# DomainsV1AvailabilityAvailabilityResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name, &#x60;null&#x60; when not claimed free domain | [optional] [default to undefined]
**is_available** | **boolean** | &#x60;true&#x60; if domain is available for registration | [optional] [default to undefined]
**is_alternative** | **boolean** | &#x60;true&#x60; if domain is provided as an alternative | [optional] [default to undefined]
**restriction** | **string** | Special rules and/or restrictions applied for registering TLD | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1AvailabilityAvailabilityResource } from 'hostinger-api-sdk';

const instance: DomainsV1AvailabilityAvailabilityResource = {
    domain,
    is_available,
    is_alternative,
    restriction,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
