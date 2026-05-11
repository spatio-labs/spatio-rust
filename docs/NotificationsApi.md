# \NotificationsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_notification_preferences**](NotificationsApi.md#get_notification_preferences) | **GET** /v1/notifications/preferences | Read the caller's notification preferences.
[**update_notification_preferences**](NotificationsApi.md#update_notification_preferences) | **PATCH** /v1/notifications/preferences | Update notification preferences.



## get_notification_preferences

> std::collections::HashMap<String, serde_json::Value> get_notification_preferences()
Read the caller's notification preferences.

### Parameters

This endpoint does not need any parameter.

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_notification_preferences

> std::collections::HashMap<String, serde_json::Value> update_notification_preferences(request_body)
Update notification preferences.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

