# \MiscApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_pinned_platform**](MiscApi.md#delete_pinned_platform) | **DELETE** /v1/pinned-platforms/{platformId} | Unpin a platform.
[**get_bootstrap**](MiscApi.md#get_bootstrap) | **GET** /v1/bootstrap | Single-shot identity + config bundle the renderer hits on first load. Replaces the legacy server-side hydration in app/layout.tsx. 
[**get_onboarding_invitations**](MiscApi.md#get_onboarding_invitations) | **GET** /v1/onboarding/invitations | Pending invitations the caller can accept during onboarding.
[**get_pinned_platforms**](MiscApi.md#get_pinned_platforms) | **GET** /v1/pinned-platforms | Read the caller's pinned-platform list (sidebar order).
[**get_platform_preferences**](MiscApi.md#get_platform_preferences) | **GET** /v1/platform-preferences | Read the caller's per-platform sidebar/visibility preferences.
[**get_platform_settings_legacy**](MiscApi.md#get_platform_settings_legacy) | **GET** /v1/settings/platform | Legacy admin-tier platform settings read endpoint.
[**get_threads_status**](MiscApi.md#get_threads_status) | **GET** /v1/threads/status | Async-thread / job-runner status snapshot.
[**get_user_permissions**](MiscApi.md#get_user_permissions) | **GET** /v1/user/permissions | Read the caller's effective per-resource permissions.
[**get_workspace_activity**](MiscApi.md#get_workspace_activity) | **GET** /v1/workspace-activity | Recent activity feed for a workspace.
[**get_workspace_layout**](MiscApi.md#get_workspace_layout) | **GET** /v1/layout/{workspaceId} | Read the renderer's saved pane layout for a workspace.
[**put_pinned_platform**](MiscApi.md#put_pinned_platform) | **PUT** /v1/pinned-platforms | Pin a platform.
[**put_platform_preferences**](MiscApi.md#put_platform_preferences) | **PUT** /v1/platform-preferences | Replace the caller's platform preferences.
[**put_workspace_layout**](MiscApi.md#put_workspace_layout) | **PUT** /v1/layout/{workspaceId} | Save the renderer's pane layout.
[**reorder_pinned_platforms**](MiscApi.md#reorder_pinned_platforms) | **POST** /v1/pinned-platforms/reorder | Reorder the pinned-platform list.
[**reset_platform_preferences**](MiscApi.md#reset_platform_preferences) | **POST** /v1/platform-preferences/reset | Reset platform preferences to defaults.
[**update_user_profile**](MiscApi.md#update_user_profile) | **PATCH** /v1/user/profile | Update the caller's user profile (name, avatar, etc.).
[**validate_organization_slug**](MiscApi.md#validate_organization_slug) | **GET** /v1/validate-slug/organization | Check whether an org slug is available.
[**validate_workspace_slug**](MiscApi.md#validate_workspace_slug) | **GET** /v1/validate-slug/workspace | Check whether a workspace slug is available.



## delete_pinned_platform

> delete_pinned_platform(platform_id)
Unpin a platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_bootstrap

> std::collections::HashMap<String, serde_json::Value> get_bootstrap()
Single-shot identity + config bundle the renderer hits on first load. Replaces the legacy server-side hydration in app/layout.tsx. 

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


## get_onboarding_invitations

> std::collections::HashMap<String, serde_json::Value> get_onboarding_invitations()
Pending invitations the caller can accept during onboarding.

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


## get_pinned_platforms

> std::collections::HashMap<String, serde_json::Value> get_pinned_platforms()
Read the caller's pinned-platform list (sidebar order).

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


## get_platform_preferences

> std::collections::HashMap<String, serde_json::Value> get_platform_preferences()
Read the caller's per-platform sidebar/visibility preferences.

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


## get_platform_settings_legacy

> std::collections::HashMap<String, serde_json::Value> get_platform_settings_legacy()
Legacy admin-tier platform settings read endpoint.

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


## get_threads_status

> std::collections::HashMap<String, serde_json::Value> get_threads_status()
Async-thread / job-runner status snapshot.

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


## get_user_permissions

> std::collections::HashMap<String, serde_json::Value> get_user_permissions()
Read the caller's effective per-resource permissions.

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


## get_workspace_activity

> std::collections::HashMap<String, serde_json::Value> get_workspace_activity(workspace_id, limit)
Recent activity feed for a workspace.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_workspace_layout

> std::collections::HashMap<String, serde_json::Value> get_workspace_layout(workspace_id)
Read the renderer's saved pane layout for a workspace.

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


## put_pinned_platform

> put_pinned_platform(request_body)
Pin a platform.

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


## put_platform_preferences

> put_platform_preferences(request_body)
Replace the caller's platform preferences.

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


## put_workspace_layout

> put_workspace_layout(workspace_id, request_body)
Save the renderer's pane layout.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reorder_pinned_platforms

> reorder_pinned_platforms(request_body)
Reorder the pinned-platform list.

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


## reset_platform_preferences

> reset_platform_preferences()
Reset platform preferences to defaults.

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


## update_user_profile

> std::collections::HashMap<String, serde_json::Value> update_user_profile(request_body)
Update the caller's user profile (name, avatar, etc.).

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


## validate_organization_slug

> std::collections::HashMap<String, serde_json::Value> validate_organization_slug(slug)
Check whether an org slug is available.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**slug** | Option<**String**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_workspace_slug

> std::collections::HashMap<String, serde_json::Value> validate_workspace_slug(slug, organization_id)
Check whether a workspace slug is available.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**slug** | Option<**String**> |  |  |
**organization_id** | Option<**String**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

