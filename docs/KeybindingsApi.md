# \KeybindingsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_key_binding**](KeybindingsApi.md#delete_key_binding) | **DELETE** /v1/keybindings/{id} | Reset a binding to its platform default.
[**get_default_key_bindings**](KeybindingsApi.md#get_default_key_bindings) | **GET** /v1/keybindings/defaults | Platform default key bindings (no user customizations applied).
[**list_key_bindings**](KeybindingsApi.md#list_key_bindings) | **GET** /v1/keybindings | User's merged key bindings (defaults + customizations).
[**reset_all_key_bindings**](KeybindingsApi.md#reset_all_key_bindings) | **POST** /v1/keybindings/reset | Reset every customization to its platform default.
[**update_key_binding**](KeybindingsApi.md#update_key_binding) | **PUT** /v1/keybindings/{id} | Create or update a user key-binding customization.
[**validate_key_binding**](KeybindingsApi.md#validate_key_binding) | **POST** /v1/keybindings/validate | Check whether a proposed binding conflicts with existing ones.



## delete_key_binding

> delete_key_binding(id)
Reset a binding to its platform default.

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


## get_default_key_bindings

> models::KeyBindingListResponse get_default_key_bindings()
Platform default key bindings (no user customizations applied).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::KeyBindingListResponse**](KeyBindingListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_key_bindings

> models::KeyBindingListResponse list_key_bindings()
User's merged key bindings (defaults + customizations).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::KeyBindingListResponse**](KeyBindingListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reset_all_key_bindings

> reset_all_key_bindings()
Reset every customization to its platform default.

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


## update_key_binding

> models::KeyBinding update_key_binding(id, update_key_binding_request)
Create or update a user key-binding customization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_key_binding_request** | [**UpdateKeyBindingRequest**](UpdateKeyBindingRequest.md) |  | [required] |

### Return type

[**models::KeyBinding**](KeyBinding.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_key_binding

> models::ValidateKeyBindingResponse validate_key_binding(validate_key_binding_request)
Check whether a proposed binding conflicts with existing ones.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_key_binding_request** | [**ValidateKeyBindingRequest**](ValidateKeyBindingRequest.md) |  | [required] |

### Return type

[**models::ValidateKeyBindingResponse**](ValidateKeyBindingResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

