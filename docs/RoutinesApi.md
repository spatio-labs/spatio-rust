# \RoutinesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**claim_routine_run**](RoutinesApi.md#claim_routine_run) | **POST** /v1/routines/runs/{id}/claim | Worker claims a queued run.
[**complete_routine_run**](RoutinesApi.md#complete_routine_run) | **POST** /v1/routines/runs/{id}/complete | Worker marks a run complete.
[**create_routine**](RoutinesApi.md#create_routine) | **POST** /v1/routines | Create a routine.
[**delete_routine**](RoutinesApi.md#delete_routine) | **DELETE** /v1/routines/{id} | Delete a routine.
[**get_routine**](RoutinesApi.md#get_routine) | **GET** /v1/routines/{id} | Fetch a routine.
[**list_routine_runs**](RoutinesApi.md#list_routine_runs) | **GET** /v1/routines/{id}/runs | List runs for a routine.
[**list_routines**](RoutinesApi.md#list_routines) | **GET** /v1/routines | List routines for the caller's workspace.
[**run_routine_now**](RoutinesApi.md#run_routine_now) | **POST** /v1/routines/{id}/run-now | Trigger an ad-hoc run.
[**update_routine**](RoutinesApi.md#update_routine) | **PATCH** /v1/routines/{id} | Update a routine.
[**update_routine_run_progress**](RoutinesApi.md#update_routine_run_progress) | **POST** /v1/routines/runs/{id}/progress | Worker reports progress.



## claim_routine_run

> models::RoutineRun claim_routine_run(id)
Worker claims a queued run.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## complete_routine_run

> models::RoutineRun complete_routine_run(id, routine_run_complete_request)
Worker marks a run complete.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**routine_run_complete_request** | [**RoutineRunCompleteRequest**](RoutineRunCompleteRequest.md) |  | [required] |

### Return type

[**models::RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_routine

> models::Routine create_routine(create_routine_request)
Create a routine.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_routine_request** | [**CreateRoutineRequest**](CreateRoutineRequest.md) |  | [required] |

### Return type

[**models::Routine**](Routine.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_routine

> delete_routine(id)
Delete a routine.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_routine

> models::Routine get_routine(id)
Fetch a routine.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::Routine**](Routine.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_routine_runs

> models::RoutineRunListResponse list_routine_runs(id)
List runs for a routine.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::RoutineRunListResponse**](RoutineRunListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_routines

> models::RoutineListResponse list_routines(workspace_id, status)
List routines for the caller's workspace.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | Option<**String**> |  |  |
**status** | Option<**String**> |  |  |

### Return type

[**models::RoutineListResponse**](RoutineListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## run_routine_now

> models::RoutineRun run_routine_now(id)
Trigger an ad-hoc run.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_routine

> models::Routine update_routine(id, update_routine_request)
Update a routine.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_routine_request** | [**UpdateRoutineRequest**](UpdateRoutineRequest.md) |  | [required] |

### Return type

[**models::Routine**](Routine.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_routine_run_progress

> models::RoutineRun update_routine_run_progress(id, routine_run_progress_request)
Worker reports progress.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**routine_run_progress_request** | [**RoutineRunProgressRequest**](RoutineRunProgressRequest.md) |  | [required] |

### Return type

[**models::RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

