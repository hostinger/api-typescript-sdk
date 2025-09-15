# VPSV1BackupBackupResource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **number** | Backup ID | [optional] [default to undefined]
**size** | **number** | Backup size in kilobytes | [optional] [default to undefined]
**restore_time** | **number** | Estimated backup restore time in seconds | [optional] [default to undefined]
**location** | **string** | Location of the backup | [optional] [default to undefined]
**created_at** | **string** |  | [optional] [default to undefined]

## Example

```typescript
import { VPSV1BackupBackupResource } from 'hostinger-api-sdk';

const instance: VPSV1BackupBackupResource = {
    id,
    size,
    restore_time,
    location,
    created_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
