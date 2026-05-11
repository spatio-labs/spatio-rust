# \SettingsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_update_settings**](SettingsApi.md#bulk_update_settings) | **POST** /v1/settings/bulk-update | Bulk-update multiple settings rows in one round-trip.
[**delete_current_user_settings**](SettingsApi.md#delete_current_user_settings) | **DELETE** /v1/settings | Reset the caller's user-level settings.
[**get_current_user_settings**](SettingsApi.md#get_current_user_settings) | **GET** /v1/settings | Fetch the caller's user-level settings.
[**get_mail_read_receipts_pref**](SettingsApi.md#get_mail_read_receipts_pref) | **GET** /v1/me/preferences/mail-read-receipts | Read the caller's mail-read-receipts preference.
[**get_settings_permissions**](SettingsApi.md#get_settings_permissions) | **GET** /v1/settings/permissions | Read the caller's settings-write permissions matrix.
[**get_user_settings**](SettingsApi.md#get_user_settings) | **GET** /v1/settings/user/{userId} | Fetch a specific user's settings (admin / self only).
[**get_workspace_settings**](SettingsApi.md#get_workspace_settings) | **GET** /v1/settings/workspace/{workspaceId} | Fetch workspace-level settings.
[**put_current_user_settings**](SettingsApi.md#put_current_user_settings) | **PUT** /v1/settings | Replace the caller's user-level settings.
[**put_mail_read_receipts_pref**](SettingsApi.md#put_mail_read_receipts_pref) | **PUT** /v1/me/preferences/mail-read-receipts | Update the caller's mail-read-receipts preference.
[**put_user_settings**](SettingsApi.md#put_user_settings) | **PUT** /v1/settings/user/{userId} | Replace a specific user's settings.
[**put_workspace_settings**](SettingsApi.md#put_workspace_settings) | **PUT** /v1/settings/workspace/{workspaceId} | Replace workspace-level settings.



## bulk_update_settings

> std::collections::HashMap<String, serde_json::Value> bulk_update_settings(request_body)
Bulk-update multiple settings rows in one round-trip.

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


## delete_current_user_settings

> delete_current_user_settings()
Reset the caller's user-level settings.

### Parameters

This endpoint does not need any parameter.

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_current_user_settings

> std::collections::HashMap<String, serde_json::Value> get_current_user_settings()
Fetch the caller's user-level settings.

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


## get_mail_read_receipts_pref

> std::collections::HashMap<String, serde_json::Value> get_mail_read_receipts_pref()
Read the caller's mail-read-receipts preference.

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


## get_settings_permissions

> std::collections::HashMap<String, serde_json::Value> get_settings_permissions()
Read the caller's settings-write permissions matrix.

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


## get_user_settings

> std::collections::HashMap<String, serde_json::Value> get_user_settings(user_id)
Fetch a specific user's settings (admin / self only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_workspace_settings

> std::collections::HashMap<String, serde_json::Value> get_workspace_settings(workspace_id)
Fetch workspace-level settings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## put_current_user_settings

> std::collections::HashMap<String, serde_json::Value> put_current_user_settings(request_body)
Replace the caller's user-level settings.

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


## put_mail_read_receipts_pref

> put_mail_read_receipts_pref(request_body)
Update the caller's mail-read-receipts preference.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## put_user_settings

> std::collections::HashMap<String, serde_json::Value> put_user_settings(user_id, request_body)
Replace a specific user's settings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**user_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## put_workspace_settings

> std::collections::HashMap<String, serde_json::Value> put_workspace_settings(workspace_id, request_body)
Replace workspace-level settings.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

