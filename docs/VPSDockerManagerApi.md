# VPSDockerManagerApi

All URIs are relative to *https://developers.hostinger.com*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**createNewProjectV1**](#createnewprojectv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/docker | Create new project|
|[**deleteProjectV1**](#deleteprojectv1) | **DELETE** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName}/down | Delete project|
|[**getProjectContainersV1**](#getprojectcontainersv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName}/containers | Get project containers|
|[**getProjectContentsV1**](#getprojectcontentsv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName} | Get project contents|
|[**getProjectListV1**](#getprojectlistv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/docker | Get project list|
|[**getProjectLogsV1**](#getprojectlogsv1) | **GET** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName}/logs | Get project logs|
|[**restartProjectV1**](#restartprojectv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName}/restart | Restart project|
|[**startProjectV1**](#startprojectv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName}/start | Start project|
|[**stopProjectV1**](#stopprojectv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName}/stop | Stop project|
|[**updateProjectV1**](#updateprojectv1) | **POST** /api/vps/v1/virtual-machines/{virtualMachineId}/docker/{projectName}/update | Update project|

# **createNewProjectV1**
> VPSV1ActionActionResource createNewProjectV1(vPSV1VirtualMachineDockerManagerUpRequest)

Deploy new project from docker-compose.yaml contents or download contents from URL.   URL can be Github repository url in format https://github.com/[user]/[repo] and it will be automatically resolved to  docker-compose.yaml file in master branch. Any other URL provided must return docker-compose.yaml file contents.  If project already exists, it will be replaced.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration,
    VPSV1VirtualMachineDockerManagerUpRequest
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let vPSV1VirtualMachineDockerManagerUpRequest: VPSV1VirtualMachineDockerManagerUpRequest; //

const { status, data } = await apiInstance.createNewProjectV1(
    virtualMachineId,
    vPSV1VirtualMachineDockerManagerUpRequest
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **vPSV1VirtualMachineDockerManagerUpRequest** | **VPSV1VirtualMachineDockerManagerUpRequest**|  | |
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deleteProjectV1**
> VPSV1ActionActionResource deleteProjectV1()

Completely removes a Docker Compose project from the virtual machine, stopping all containers and cleaning up  associated resources including networks, volumes, and images.   This operation is irreversible and will delete all project data.   Use this when you want to permanently remove a project and free up system resources.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.deleteProjectV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectContainersV1**
> Array<VPSV1DockerManagerContainerResource> getProjectContainersV1()

Retrieves a list of all containers belonging to a specific Docker Compose project on the virtual machine.   This endpoint returns detailed information about each container including their current status, port mappings, and runtime configuration.   Use this to monitor the health and state of all services within your Docker Compose project.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.getProjectContainersV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**Array<VPSV1DockerManagerContainerResource>**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectContentsV1**
> VPSV1DockerManagerContentResource getProjectContentsV1()

Retrieves the complete project information including the docker-compose.yml file contents, project metadata, and current deployment status.   This endpoint provides the full configuration and state details of a specific Docker Compose project.   Use this to inspect project settings, review the compose file, or check the overall project health.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.getProjectContentsV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**VPSV1DockerManagerContentResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectListV1**
> Array<VPSV1DockerManagerProjectResource> getProjectListV1()

Retrieves a list of all Docker Compose projects currently deployed on the virtual machine.   This endpoint returns basic information about each project including name, status, and file path.   Use this to get an overview of all Docker projects on your VPS instance.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)

const { status, data } = await apiInstance.getProjectListV1(
    virtualMachineId
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|


### Return type

**Array<VPSV1DockerManagerProjectResource>**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getProjectLogsV1**
> Array<VPSV1DockerManagerLogsResource> getProjectLogsV1()

Retrieves aggregated log entries from all services within a Docker Compose project.   This endpoint returns recent log output from each container, organized by service name with timestamps.  The response contains the last 300 log entries across all services.   Use this for debugging, monitoring application behavior, and troubleshooting issues across your entire project stack.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.getProjectLogsV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**Array<VPSV1DockerManagerLogsResource>**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restartProjectV1**
> VPSV1ActionActionResource restartProjectV1()

Restarts all services in a Docker Compose project by stopping and starting containers in the correct dependency order.   This operation preserves data volumes and network configurations while refreshing the running containers.   Use this to apply configuration changes or recover from service failures.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.restartProjectV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **startProjectV1**
> VPSV1ActionActionResource startProjectV1()

Starts all services in a Docker Compose project that are currently stopped.   This operation brings up containers in the correct dependency order as defined in the compose file.   Use this to resume a project that was previously stopped or to start services after a system reboot.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.startProjectV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stopProjectV1**
> VPSV1ActionActionResource stopProjectV1()

Stops all running services in a Docker Compose project while preserving container configurations and data volumes.   This operation gracefully shuts down containers in reverse dependency order.   Use this to temporarily halt a project without removing data or configurations.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.stopProjectV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **updateProjectV1**
> VPSV1ActionActionResource updateProjectV1()

Updates a Docker Compose project by pulling the latest image versions and recreating containers with new configurations.   This operation preserves data volumes while applying changes from the compose file.   Use this to deploy application updates, apply configuration changes, or refresh container images to their latest versions.

### Example

```typescript
import {
    VPSDockerManagerApi,
    Configuration
} from 'hostinger-api-sdk';

const configuration = new Configuration();
const apiInstance = new VPSDockerManagerApi(configuration);

let virtualMachineId: number; //Virtual Machine ID (default to undefined)
let projectName: string; //Docker Compose project name using alphanumeric characters, dashes, and underscores only (default to undefined)

const { status, data } = await apiInstance.updateProjectV1(
    virtualMachineId,
    projectName
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **virtualMachineId** | [**number**] | Virtual Machine ID | defaults to undefined|
| **projectName** | [**string**] | Docker Compose project name using alphanumeric characters, dashes, and underscores only | defaults to undefined|


### Return type

**VPSV1ActionActionResource**

### Authorization

[apiToken](../README.md#apiToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Success response |  -  |
|**422** | Validation error response |  -  |
|**401** | Unauthenticated response |  -  |
|**500** | Error response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

