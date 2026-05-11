# \PlatformsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_platform_provider_account**](PlatformsApi.md#add_platform_provider_account) | **POST** /v1/platforms/{platformId}/providers/{provider}/accounts | Add a connected account for a platform/provider pair.
[**create_or_update_platform_secret**](PlatformsApi.md#create_or_update_platform_secret) | **POST** /v1/platforms/{platformId}/secrets | Create or update a secret value.
[**delete_platform_secret**](PlatformsApi.md#delete_platform_secret) | **DELETE** /v1/platforms/{platformId}/secrets/{name} | Delete a secret.
[**exec_platform_data**](PlatformsApi.md#exec_platform_data) | **POST** /v1/platforms/{platformId}/exec | Run an INSERT/UPDATE/DELETE statement against a platform's store.
[**export_platform_secrets**](PlatformsApi.md#export_platform_secrets) | **GET** /v1/platforms/{platformId}/secrets/export | Export all secrets for a platform (values included). Caller must be the platform owner. 
[**generate_platform_backend_token**](PlatformsApi.md#generate_platform_backend_token) | **POST** /v1/platforms/{platformId}/backend-token | Generate a short-lived backend JWT a platform's worker can use to call back into platform-service. 
[**get_platform_catalog**](PlatformsApi.md#get_platform_catalog) | **GET** /v1/catalog/platforms | List the global platform catalog — every platform that exists, not just the ones the caller has installed. 
[**get_platform_manifest**](PlatformsApi.md#get_platform_manifest) | **GET** /v1/platforms/{platformId}/manifest | Fetch a platform's manifest (capabilities, schema, UI metadata).
[**list_platform_accounts**](PlatformsApi.md#list_platform_accounts) | **GET** /v1/platforms/{platformId}/accounts | List accounts the caller has connected for a platform.
[**list_platform_providers**](PlatformsApi.md#list_platform_providers) | **GET** /v1/platforms/{platformId}/providers | Discover supported providers + capabilities for a platform.
[**list_platform_secrets**](PlatformsApi.md#list_platform_secrets) | **GET** /v1/platforms/{platformId}/secrets | List secret keys (values redacted).
[**list_platform_tables**](PlatformsApi.md#list_platform_tables) | **GET** /v1/platforms/{platformId}/tables | List tables in a platform's data store.
[**list_platforms**](PlatformsApi.md#list_platforms) | **GET** /v1/platforms | List installed platforms for the sidebar.
[**query_platform_data**](PlatformsApi.md#query_platform_data) | **POST** /v1/platforms/{platformId}/query | Run a SELECT query against a platform's data store.
[**run_platform_migrations**](PlatformsApi.md#run_platform_migrations) | **POST** /v1/platforms/{platformId}/migrate | Run pending migrations for a platform.



## add_platform_provider_account

> std::collections::HashMap<String, serde_json::Value> add_platform_provider_account(platform_id, provider, request_body)
Add a connected account for a platform/provider pair.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |
**provider** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_or_update_platform_secret

> std::collections::HashMap<String, serde_json::Value> create_or_update_platform_secret(platform_id, request_body)
Create or update a secret value.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_platform_secret

> delete_platform_secret(platform_id, name)
Delete a secret.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |
**name** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## exec_platform_data

> std::collections::HashMap<String, serde_json::Value> exec_platform_data(platform_id, request_body)
Run an INSERT/UPDATE/DELETE statement against a platform's store.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## export_platform_secrets

> std::collections::HashMap<String, serde_json::Value> export_platform_secrets(platform_id)
Export all secrets for a platform (values included). Caller must be the platform owner. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## generate_platform_backend_token

> std::collections::HashMap<String, serde_json::Value> generate_platform_backend_token(platform_id)
Generate a short-lived backend JWT a platform's worker can use to call back into platform-service. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_platform_catalog

> std::collections::HashMap<String, serde_json::Value> get_platform_catalog()
List the global platform catalog — every platform that exists, not just the ones the caller has installed. 

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


## get_platform_manifest

> std::collections::HashMap<String, serde_json::Value> get_platform_manifest(platform_id)
Fetch a platform's manifest (capabilities, schema, UI metadata).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_platform_accounts

> std::collections::HashMap<String, serde_json::Value> list_platform_accounts(platform_id)
List accounts the caller has connected for a platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_platform_providers

> std::collections::HashMap<String, serde_json::Value> list_platform_providers(platform_id)
Discover supported providers + capabilities for a platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_platform_secrets

> std::collections::HashMap<String, serde_json::Value> list_platform_secrets(platform_id)
List secret keys (values redacted).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_platform_tables

> std::collections::HashMap<String, serde_json::Value> list_platform_tables(platform_id)
List tables in a platform's data store.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_platforms

> std::collections::HashMap<String, serde_json::Value> list_platforms()
List installed platforms for the sidebar.

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


## query_platform_data

> std::collections::HashMap<String, serde_json::Value> query_platform_data(platform_id, request_body)
Run a SELECT query against a platform's data store.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## run_platform_migrations

> std::collections::HashMap<String, serde_json::Value> run_platform_migrations(platform_id)
Run pending migrations for a platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

