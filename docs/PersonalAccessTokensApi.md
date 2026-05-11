# \PersonalAccessTokensApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_personal_access_token**](PersonalAccessTokensApi.md#create_personal_access_token) | **POST** /v1/tokens | Create a new PAT. The full token is returned only once on creation; the API never reveals the secret again. 
[**list_available_pat_scopes**](PersonalAccessTokensApi.md#list_available_pat_scopes) | **GET** /v1/tokens/scopes | List the scope strings PATs can be issued with.
[**list_personal_access_tokens**](PersonalAccessTokensApi.md#list_personal_access_tokens) | **GET** /v1/tokens | List the caller's personal access tokens (with available scopes).
[**revoke_personal_access_token**](PersonalAccessTokensApi.md#revoke_personal_access_token) | **DELETE** /v1/tokens/{id} | Revoke a PAT.
[**update_personal_access_token**](PersonalAccessTokensApi.md#update_personal_access_token) | **PATCH** /v1/tokens/{id} | Rename or re-describe a PAT (scopes are immutable).
[**workspace_create_pat**](PersonalAccessTokensApi.md#workspace_create_pat) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tokens | 
[**workspace_list_pats**](PersonalAccessTokensApi.md#workspace_list_pats) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tokens | 
[**workspace_revoke_pat**](PersonalAccessTokensApi.md#workspace_revoke_pat) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/tokens/{id} | 
[**workspace_update_pat**](PersonalAccessTokensApi.md#workspace_update_pat) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/tokens/{id} | 



## create_personal_access_token

> models::CreatePatResponse create_personal_access_token(create_pat_request)
Create a new PAT. The full token is returned only once on creation; the API never reveals the secret again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_pat_request** | [**CreatePatRequest**](CreatePatRequest.md) |  | [required] |

### Return type

[**models::CreatePatResponse**](CreatePATResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_available_pat_scopes

> models::PatScopesResponse list_available_pat_scopes()
List the scope strings PATs can be issued with.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::PatScopesResponse**](PATScopesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_personal_access_tokens

> models::PatListResponse list_personal_access_tokens()
List the caller's personal access tokens (with available scopes).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::PatListResponse**](PATListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_personal_access_token

> revoke_personal_access_token(id)
Revoke a PAT.

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


## update_personal_access_token

> models::PersonalAccessToken update_personal_access_token(id, update_pat_request)
Rename or re-describe a PAT (scopes are immutable).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_pat_request** | [**UpdatePatRequest**](UpdatePatRequest.md) |  | [required] |

### Return type

[**models::PersonalAccessToken**](PersonalAccessToken.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_create_pat

> std::collections::HashMap<String, serde_json::Value> workspace_create_pat(org, workspace, request_body)


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


## workspace_list_pats

> std::collections::HashMap<String, serde_json::Value> workspace_list_pats(org, workspace)


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


## workspace_revoke_pat

> workspace_revoke_pat(org, workspace, id)


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


## workspace_update_pat

> std::collections::HashMap<String, serde_json::Value> workspace_update_pat(org, workspace, id, request_body)


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

