# \CalendarApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_calendar_event**](CalendarApi.md#create_calendar_event) | **POST** /v1/calendar/events | Create a calendar event.
[**delete_calendar_event**](CalendarApi.md#delete_calendar_event) | **DELETE** /v1/calendar/events/{id} | Delete an event.
[**get_calendar_capabilities**](CalendarApi.md#get_calendar_capabilities) | **GET** /v1/calendar/capabilities | Per-account capability flags.
[**get_calendar_event**](CalendarApi.md#get_calendar_event) | **GET** /v1/calendar/events/{id} | Fetch one event.
[**list_calendar_events**](CalendarApi.md#list_calendar_events) | **GET** /v1/calendar/events | List calendar events across connected accounts.
[**list_calendar_providers**](CalendarApi.md#list_calendar_providers) | **GET** /v1/calendar/providers | List supported calendar providers.
[**sync_calendar**](CalendarApi.md#sync_calendar) | **POST** /v1/calendar/sync | Trigger a sync across connected calendar accounts.
[**update_calendar_event**](CalendarApi.md#update_calendar_event) | **PATCH** /v1/calendar/events/{id} | Update an event (sparse).
[**workspace_create_calendar_event**](CalendarApi.md#workspace_create_calendar_event) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calendar/events | Workspace-scoped create-event (RBAC-protected).
[**workspace_delete_calendar_event**](CalendarApi.md#workspace_delete_calendar_event) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} | 
[**workspace_get_calendar_event**](CalendarApi.md#workspace_get_calendar_event) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} | 
[**workspace_list_calendar_events**](CalendarApi.md#workspace_list_calendar_events) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/events | Workspace-scoped list-events (RBAC-protected).
[**workspace_list_calendar_providers**](CalendarApi.md#workspace_list_calendar_providers) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/providers | Workspace-scoped calendar providers.
[**workspace_update_calendar_event**](CalendarApi.md#workspace_update_calendar_event) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} | 



## create_calendar_event

> models::CreateCalendarEvent201Response create_calendar_event(create_event_request, x_workspace_id)
Create a calendar event.

Single-account create. `account_id` is required (no auto-resolve for write operations). Reminder array is mirrored into native tasks under the hood; conference data is auto-attached when `conference_type` is supplied. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_event_request** | [**CreateEventRequest**](CreateEventRequest.md) |  | [required] |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::CreateCalendarEvent201Response**](createCalendarEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_calendar_event

> models::CalendarOperationResult delete_calendar_event(id, account_id, x_workspace_id)
Delete an event.

Hard delete (no soft-delete / trash). Cascades to any reminder tasks the platform created from this event. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Event id. | [required] |
**account_id** | **String** | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations.  | [required] |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::CalendarOperationResult**](CalendarOperationResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_calendar_capabilities

> models::CalendarCapabilitiesResponse get_calendar_capabilities(account_id)
Per-account capability flags.

Returns the capabilities the provider declares for the given connected account. The renderer uses these to enable/disable form fields (recurrence picker, attendee inputs, etc.). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations.  | [required] |

### Return type

[**models::CalendarCapabilitiesResponse**](CalendarCapabilitiesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_calendar_event

> models::SpatioEvent get_calendar_event(id, account_id, x_workspace_id)
Fetch one event.

Requires `?account_id=` to identify the source account. Response is the bare `Event` (not wrapped in CalendarOperationResult — distinct from the list/create/update shapes). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Event id. | [required] |
**account_id** | **String** | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations.  | [required] |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SpatioEvent**](SpatioEvent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_calendar_events

> models::ListCalendarEvents200Response list_calendar_events(account_ids, providers, x_workspace_id, time_min, time_max, limit)
List calendar events across connected accounts.

Fan-out list. Returns events across every connected calendar provider unless filtered by `account_ids[]` or `providers[]`. Supports the cross-platform repeated-or-comma-separated filter syntax (`?account_ids=a&account_ids=b` or `?account_ids=a,b`).  Time bounds (`timeMin` / `timeMax`) accept both RFC3339 and RFC3339Nano. The handler also accepts the snake_case `time_min` / `time_max` for direct curl callers; the spec models the camelCase form because that's what the renderer and SDKs use. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to specific connected accounts. |  |
**providers** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to provider ids (`google-calendar`, etc.). |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**time_min** | Option<**chrono::DateTime<chrono::FixedOffset>**> | Inclusive lower-bound time. RFC3339 or RFC3339Nano. |  |
**time_max** | Option<**chrono::DateTime<chrono::FixedOffset>**> | Inclusive upper-bound time. |  |
**limit** | Option<**i32**> | Max events to return per page (default 50). |  |[default to 50]

### Return type

[**models::ListCalendarEvents200Response**](listCalendarEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_calendar_providers

> models::CalendarProvidersInfo list_calendar_providers()
List supported calendar providers.

Static list of provider ids the Calendar platform can connect to. Returned regardless of which providers the caller has actually authorized. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::CalendarProvidersInfo**](CalendarProvidersInfo.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## sync_calendar

> models::CalendarSyncResponse sync_calendar(wait)
Trigger a sync across connected calendar accounts.

Enqueues sync jobs (one per connected calendar account) and returns immediately with the job ids. Pass `?wait=true` to block until all jobs complete (10-second polling budget); the response is then `200` with `waited: true` and a `timed_out` flag if any job didn't finish in time. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**wait** | Option<**bool**> | Block until all sync jobs finish (10s timeout). |  |[default to false]

### Return type

[**models::CalendarSyncResponse**](CalendarSyncResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_calendar_event

> models::CreateCalendarEvent201Response update_calendar_event(id, update_event_request, x_workspace_id, account_id)
Update an event (sparse).

Partial update. `account_id` may be supplied in the body (preferred) or as `?account_id=` query param — the renderer's update path puts it in the URL while create puts it in the body. `updates` is a free-form map; the platform's capability gate rejects fields the provider doesn't support. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Event id. | [required] |
**update_event_request** | [**UpdateEventRequest**](UpdateEventRequest.md) |  | [required] |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**account_id** | Option<**String**> | Optional account-id filter (snake_case). |  |

### Return type

[**models::CreateCalendarEvent201Response**](createCalendarEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_create_calendar_event

> std::collections::HashMap<String, serde_json::Value> workspace_create_calendar_event(org, workspace, request_body)
Workspace-scoped create-event (RBAC-protected).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_delete_calendar_event

> workspace_delete_calendar_event(org, workspace, id)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_get_calendar_event

> std::collections::HashMap<String, serde_json::Value> workspace_get_calendar_event(org, workspace, id)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_list_calendar_events

> std::collections::HashMap<String, serde_json::Value> workspace_list_calendar_events(org, workspace)
Workspace-scoped list-events (RBAC-protected).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_list_calendar_providers

> std::collections::HashMap<String, serde_json::Value> workspace_list_calendar_providers(org, workspace)
Workspace-scoped calendar providers.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_update_calendar_event

> std::collections::HashMap<String, serde_json::Value> workspace_update_calendar_event(org, workspace, id, request_body)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

