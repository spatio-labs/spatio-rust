# \ConnectionsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**disconnect_connection**](ConnectionsApi.md#disconnect_connection) | **POST** /v1/connections/disconnect | Disconnect a connected account.
[**install_connection**](ConnectionsApi.md#install_connection) | **POST** /v1/connections/install | Begin an OAuth install for a connection.
[**list_accounts**](ConnectionsApi.md#list_accounts) | **GET** /v1/accounts | List the caller's multi-provider accounts.
[**list_connection_integrations**](ConnectionsApi.md#list_connection_integrations) | **GET** /v1/connections/integrations | List supported integrations + their connection state. Legacy path; `/v1/connections/list` is the preferred alias. 
[**list_connections**](ConnectionsApi.md#list_connections) | **GET** /v1/connections/list | List supported integrations + their connection state.
[**list_user_connections**](ConnectionsApi.md#list_user_connections) | **GET** /v1/connections/user | List the caller's connected accounts.
[**refresh_connection**](ConnectionsApi.md#refresh_connection) | **POST** /v1/connections/refresh | Force a refresh of a connection's OAuth tokens.
[**remove_account**](ConnectionsApi.md#remove_account) | **DELETE** /v1/accounts/{accountId} | Remove an account.
[**resolve_account**](ConnectionsApi.md#resolve_account) | **GET** /v1/accounts/resolve | Resolve an account by provider/identifier.
[**sync_account**](ConnectionsApi.md#sync_account) | **POST** /v1/accounts/{accountId}/sync | Force a sync against the upstream provider.
[**update_account**](ConnectionsApi.md#update_account) | **PATCH** /v1/accounts/{accountId} | Update account metadata (label, etc.).



## disconnect_connection

> std::collections::HashMap<String, serde_json::Value> disconnect_connection(disconnect_connection_request)
Disconnect a connected account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**disconnect_connection_request** | [**DisconnectConnectionRequest**](DisconnectConnectionRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## install_connection

> std::collections::HashMap<String, serde_json::Value> install_connection(install_connection_request)
Begin an OAuth install for a connection.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**install_connection_request** | [**InstallConnectionRequest**](InstallConnectionRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_accounts

> models::AccountListResponse list_accounts()
List the caller's multi-provider accounts.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AccountListResponse**](AccountListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_connection_integrations

> models::ConnectionListResponse list_connection_integrations()
List supported integrations + their connection state. Legacy path; `/v1/connections/list` is the preferred alias. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ConnectionListResponse**](ConnectionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_connections

> models::ConnectionListResponse list_connections()
List supported integrations + their connection state.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ConnectionListResponse**](ConnectionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_user_connections

> models::ConnectionAccountListResponse list_user_connections()
List the caller's connected accounts.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ConnectionAccountListResponse**](ConnectionAccountListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## refresh_connection

> std::collections::HashMap<String, serde_json::Value> refresh_connection(refresh_connection_request)
Force a refresh of a connection's OAuth tokens.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**refresh_connection_request** | [**RefreshConnectionRequest**](RefreshConnectionRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_account

> remove_account(account_id)
Remove an account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## resolve_account

> std::collections::HashMap<String, serde_json::Value> resolve_account(provider, email)
Resolve an account by provider/identifier.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**provider** | Option<**String**> |  |  |
**email** | Option<**String**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## sync_account

> std::collections::HashMap<String, serde_json::Value> sync_account(account_id)
Force a sync against the upstream provider.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_account

> std::collections::HashMap<String, serde_json::Value> update_account(account_id, update_account_request)
Update account metadata (label, etc.).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**update_account_request** | [**UpdateAccountRequest**](UpdateAccountRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

