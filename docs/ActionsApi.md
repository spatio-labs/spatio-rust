# \ActionsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**execute_action**](ActionsApi.md#execute_action) | **POST** /v1/actions/execute | Renderer-side execute alias. The canonical endpoint is `POST /v1/agent/actions/execute`; this path delegates to the same handler. 
[**get_core_action**](ActionsApi.md#get_core_action) | **GET** /v1/actions/core/{id} | Fetch a single core action by id.
[**list_available_actions**](ActionsApi.md#list_available_actions) | **GET** /v1/actions/available | List every action the agent platform exposes.
[**list_core_actions**](ActionsApi.md#list_core_actions) | **GET** /v1/actions/core | List renderer-curated \"core actions\" (command-palette + keybindings backing).
[**list_core_actions_by_platform**](ActionsApi.md#list_core_actions_by_platform) | **GET** /v1/actions/core/platform/{platform} | Core actions filtered to one platform.
[**list_platform_actions**](ActionsApi.md#list_platform_actions) | **GET** /v1/actions/platform/{platform} | List actions tagged for a specific platform (notes, mail, ...).



## execute_action

> models::ExecuteActionResponse execute_action(execute_action_request)
Renderer-side execute alias. The canonical endpoint is `POST /v1/agent/actions/execute`; this path delegates to the same handler. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**execute_action_request** | [**ExecuteActionRequest**](ExecuteActionRequest.md) |  | [required] |

### Return type

[**models::ExecuteActionResponse**](ExecuteActionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_core_action

> models::CoreAction get_core_action(id)
Fetch a single core action by id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::CoreAction**](CoreAction.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_available_actions

> Vec<models::ActionDescriptor> list_available_actions()
List every action the agent platform exposes.

### Parameters

This endpoint does not need any parameter.

### Return type

[**Vec<models::ActionDescriptor>**](ActionDescriptor.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_core_actions

> models::CoreActionListResponse list_core_actions()
List renderer-curated \"core actions\" (command-palette + keybindings backing).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::CoreActionListResponse**](CoreActionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_core_actions_by_platform

> models::CoreActionListResponse list_core_actions_by_platform(platform)
Core actions filtered to one platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | **String** |  | [required] |

### Return type

[**models::CoreActionListResponse**](CoreActionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_platform_actions

> Vec<models::ActionDescriptor> list_platform_actions(platform)
List actions tagged for a specific platform (notes, mail, ...).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**platform** | **String** |  | [required] |

### Return type

[**Vec<models::ActionDescriptor>**](ActionDescriptor.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

