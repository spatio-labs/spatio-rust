# \AccountApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**change_password**](AccountApi.md#change_password) | **POST** /v1/account/security/password | Change or set the account password.
[**consume_agent_task**](AccountApi.md#consume_agent_task) | **POST** /v1/account/usage/consume-agent-task | Atomic check + increment on the agent-task counter (one slot per turn).
[**get_account_plan**](AccountApi.md#get_account_plan) | **GET** /v1/account/plan | The caller's subscription tier and status.
[**get_account_tier**](AccountApi.md#get_account_tier) | **GET** /v1/account/tier | Capability + quota envelope for the caller's tier.
[**get_account_usage**](AccountApi.md#get_account_usage) | **GET** /v1/account/usage | Today's usage counters across notes, sheets, slides, files, tasks, mail, API.
[**get_agent_task_usage**](AccountApi.md#get_agent_task_usage) | **GET** /v1/account/usage/agent-tasks | Free-trial agent-task counter snapshot. Read-only; does NOT consume a slot. Use POST `/v1/account/usage/consume-agent-task` atomically per turn to gate a tool-using turn. 
[**get_sign_in_methods**](AccountApi.md#get_sign_in_methods) | **GET** /v1/account/security/sign-in-methods | List the linked sign-in methods (password + OAuth providers).
[**list_connected_apps**](AccountApi.md#list_connected_apps) | **GET** /v1/account/connected-apps | List the OAuth clients the calling user has granted access to.
[**list_sessions**](AccountApi.md#list_sessions) | **GET** /v1/account/security/sessions | List active sessions for the caller.
[**revoke_connected_app**](AccountApi.md#revoke_connected_app) | **DELETE** /v1/account/connected-apps/{client_id} | Revoke a connected app and all of its active tokens.
[**revoke_other_sessions**](AccountApi.md#revoke_other_sessions) | **POST** /v1/account/security/sessions/revoke-others | Revoke every session except the caller's current one.
[**revoke_session**](AccountApi.md#revoke_session) | **DELETE** /v1/account/security/sessions/{id} | Revoke a specific session.



## change_password

> change_password(change_password_request)
Change or set the account password.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**change_password_request** | [**ChangePasswordRequest**](ChangePasswordRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## consume_agent_task

> models::ConsumeAgentTaskResponse consume_agent_task()
Atomic check + increment on the agent-task counter (one slot per turn).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ConsumeAgentTaskResponse**](ConsumeAgentTaskResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_account_plan

> models::AccountPlan get_account_plan()
The caller's subscription tier and status.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AccountPlan**](AccountPlan.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_account_tier

> models::AccountTierDetails get_account_tier()
Capability + quota envelope for the caller's tier.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AccountTierDetails**](AccountTierDetails.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_account_usage

> models::AccountUsage get_account_usage()
Today's usage counters across notes, sheets, slides, files, tasks, mail, API.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AccountUsage**](AccountUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_agent_task_usage

> models::AgentTaskUsage get_agent_task_usage()
Free-trial agent-task counter snapshot. Read-only; does NOT consume a slot. Use POST `/v1/account/usage/consume-agent-task` atomically per turn to gate a tool-using turn. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AgentTaskUsage**](AgentTaskUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sign_in_methods

> models::SignInMethods get_sign_in_methods()
List the linked sign-in methods (password + OAuth providers).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::SignInMethods**](SignInMethods.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_connected_apps

> models::ConnectedAppsListResponse list_connected_apps()
List the OAuth clients the calling user has granted access to.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ConnectedAppsListResponse**](ConnectedAppsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sessions

> models::SessionListResponse list_sessions()
List active sessions for the caller.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::SessionListResponse**](SessionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_connected_app

> revoke_connected_app(client_id)
Revoke a connected app and all of its active tokens.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**client_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_other_sessions

> models::RevokeOtherSessionsResponse revoke_other_sessions()
Revoke every session except the caller's current one.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::RevokeOtherSessionsResponse**](RevokeOtherSessionsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_session

> revoke_session(id)
Revoke a specific session.

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

