# \InboxApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_inbox_counts**](InboxApi.md#get_inbox_counts) | **GET** /v1/inbox/counts | Per-bucket unread counts.
[**list_inbox**](InboxApi.md#list_inbox) | **GET** /v1/inbox | Unified inbox feed across mail, channel mentions, DMs, system notifications.
[**mark_inbox_item_read**](InboxApi.md#mark_inbox_item_read) | **PATCH** /v1/inbox/{id}/read | Mark a single inbox item as read.
[**workspace_get_inbox_counts**](InboxApi.md#workspace_get_inbox_counts) | **GET** /v1/organizations/{org}/workspaces/{workspace}/inbox/counts | 
[**workspace_list_inbox**](InboxApi.md#workspace_list_inbox) | **GET** /v1/organizations/{org}/workspaces/{workspace}/inbox | 
[**workspace_mark_inbox_item_read**](InboxApi.md#workspace_mark_inbox_item_read) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/inbox/{id}/read | 



## get_inbox_counts

> models::InboxCounts get_inbox_counts()
Per-bucket unread counts.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::InboxCounts**](InboxCounts.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox

> models::InboxListResponse list_inbox(category, unread_only, limit)
Unified inbox feed across mail, channel mentions, DMs, system notifications.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**category** | Option<**String**> |  |  |
**unread_only** | Option<**bool**> |  |  |
**limit** | Option<**i32**> |  |  |

### Return type

[**models::InboxListResponse**](InboxListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_inbox_item_read

> mark_inbox_item_read(id)
Mark a single inbox item as read.

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


## workspace_get_inbox_counts

> std::collections::HashMap<String, serde_json::Value> workspace_get_inbox_counts(org, workspace)


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


## workspace_list_inbox

> std::collections::HashMap<String, serde_json::Value> workspace_list_inbox(org, workspace)


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


## workspace_mark_inbox_item_read

> workspace_mark_inbox_item_read(org, workspace, id)


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

