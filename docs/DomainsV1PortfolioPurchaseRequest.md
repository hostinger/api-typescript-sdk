# DomainsV1PortfolioPurchaseRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **string** | Domain name | [default to undefined]
**item_id** | **string** | Catalog price item ID | [default to undefined]
**payment_method_id** | **number** | Payment method ID, default will be used if not provided | [optional] [default to undefined]
**domain_contacts** | [**DomainsV1PortfolioPurchaseRequestDomainContacts**](DomainsV1PortfolioPurchaseRequestDomainContacts.md) |  | [optional] [default to undefined]
**additional_details** | **object** | Additional registration data, possible values depends on TLD | [optional] [default to undefined]
**coupons** | **Array&lt;any&gt;** | Discount coupon codes | [optional] [default to undefined]

## Example

```typescript
import { DomainsV1PortfolioPurchaseRequest } from 'hostinger-api-sdk';

const instance: DomainsV1PortfolioPurchaseRequest = {
    domain,
    item_id,
    payment_method_id,
    domain_contacts,
    additional_details,
    coupons,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
