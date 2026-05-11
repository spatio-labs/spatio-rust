# \TerminalApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_terminal_session**](TerminalApi.md#create_terminal_session) | **POST** /v1/terminal/sessions | Create a terminal session record. PTY bytes flow renderer ↔ local-agent over IPC and never traverse this API. 
[**delete_terminal_session**](TerminalApi.md#delete_terminal_session) | **DELETE** /v1/terminal/sessions/{id} | Delete a terminal session record.
[**get_terminal_session**](TerminalApi.md#get_terminal_session) | **GET** /v1/terminal/sessions/{id} | Fetch a terminal session.
[**list_terminal_sessions**](TerminalApi.md#list_terminal_sessions) | **GET** /v1/terminal/sessions | List the caller's terminal sessions (metadata only — no PTY bytes).
[**update_terminal_session**](TerminalApi.md#update_terminal_session) | **PATCH** /v1/terminal/sessions/{id} | Update terminal session metadata (title, cwd, etc.).



## create_terminal_session

> std::collections::HashMap<String, serde_json::Value> create_terminal_session(request_body)
Create a terminal session record. PTY bytes flow renderer ↔ local-agent over IPC and never traverse this API. 

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


## delete_terminal_session

> delete_terminal_session(id)
Delete a terminal session record.

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


## get_terminal_session

> std::collections::HashMap<String, serde_json::Value> get_terminal_session(id)
Fetch a terminal session.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_terminal_sessions

> std::collections::HashMap<String, serde_json::Value> list_terminal_sessions()
List the caller's terminal sessions (metadata only — no PTY bytes).

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


## update_terminal_session

> std::collections::HashMap<String, serde_json::Value> update_terminal_session(id, request_body)
Update terminal session metadata (title, cwd, etc.).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
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

