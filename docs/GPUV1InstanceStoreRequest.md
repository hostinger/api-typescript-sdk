# GPUV1InstanceStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pool_instance_id** | **number** | Instance type ID from the pool instance types list | [default to undefined]
**os_template_id** | **number** | OS template ID available for the selected instance type | [default to undefined]
**name** | **string** | Instance name, unique among your instances. Letters, numbers, dashes and underscores only | [default to undefined]
**public_keys** | **Array&lt;string&gt;** | SSH public keys to add to the instance | [optional] [default to undefined]

## Example

```typescript
import { GPUV1InstanceStoreRequest } from '@hostinger/sdk';

const instance: GPUV1InstanceStoreRequest = {
    pool_instance_id,
    os_template_id,
    name,
    public_keys,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
