# GPUV1PoolPoolGroupResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | GPU pool group ID | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**description** | **string** |  | [optional] [default to undefined]
**feature** | **string** |  | [optional] [default to undefined]
**vram** | **number** | Total VRAM in bytes | [optional] [default to undefined]
**is_available** | **boolean** | Whether the group has any available pools | [optional] [default to undefined]
**min_price_per_hour** | **number** | Lowest hourly price of the group instance types, in credits | [optional] [default to undefined]
**pools** | [**Array&lt;GPUV1PoolPoolResource&gt;**](GPUV1PoolPoolResource.md) | Array of [&#x60;GPU.V1.Pool.PoolResource&#x60;](#model/gpuv1poolpoolresource) | [optional] [default to undefined]

## Example

```typescript
import { GPUV1PoolPoolGroupResource } from '@hostinger/sdk';

const instance: GPUV1PoolPoolGroupResource = {
    id,
    name,
    description,
    feature,
    vram,
    is_available,
    min_price_per_hour,
    pools,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
