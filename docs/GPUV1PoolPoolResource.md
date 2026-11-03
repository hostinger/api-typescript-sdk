# GPUV1PoolPoolResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | GPU pool ID | [optional] [default to undefined]
**name** | **string** |  | [optional] [default to undefined]
**gpus** | **number** | Number of GPUs | [optional] [default to undefined]
**vram** | **number** | Total VRAM in bytes | [optional] [default to undefined]
**is_available** | **boolean** | Whether the pool has available instances for booking | [optional] [default to undefined]
**region** | [**GPUV1RegionRegionResource**](GPUV1RegionRegionResource.md) |  | [optional] [default to undefined]

## Example

```typescript
import { GPUV1PoolPoolResource } from '@hostinger/sdk';

const instance: GPUV1PoolPoolResource = {
    id,
    name,
    gpus,
    vram,
    is_available,
    region,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
