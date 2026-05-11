# \ChannelsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_channel**](ChannelsApi.md#create_channel) | **POST** /v1/channels | Create a channel.
[**execute_channel_action**](ChannelsApi.md#execute_channel_action) | **POST** /v1/channels/execute | Dispatch a channel action by id.
[**join_channel**](ChannelsApi.md#join_channel) | **POST** /v1/channels/{id}/join | Join a channel.
[**leave_channel**](ChannelsApi.md#leave_channel) | **POST** /v1/channels/{id}/leave | Leave a channel.
[**list_channel_actions**](ChannelsApi.md#list_channel_actions) | **GET** /v1/channels/actions | Discover the action catalog for the Channels platform.
[**list_channel_messages**](ChannelsApi.md#list_channel_messages) | **GET** /v1/channels/messages | List messages in a channel.
[**list_channels**](ChannelsApi.md#list_channels) | **GET** /v1/channels | List group channels across connected chat providers.
[**send_channel_message**](ChannelsApi.md#send_channel_message) | **POST** /v1/channels/messages | Send a message to a channel.
[**workspace_create_channel**](ChannelsApi.md#workspace_create_channel) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels | 
[**workspace_execute_channel_action**](ChannelsApi.md#workspace_execute_channel_action) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/execute | 
[**workspace_join_channel**](ChannelsApi.md#workspace_join_channel) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/{id}/join | 
[**workspace_leave_channel**](ChannelsApi.md#workspace_leave_channel) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/{id}/leave | 
[**workspace_list_channel_actions**](ChannelsApi.md#workspace_list_channel_actions) | **GET** /v1/organizations/{org}/workspaces/{workspace}/channels/actions | 
[**workspace_list_channel_messages**](ChannelsApi.md#workspace_list_channel_messages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/channels/messages | 
[**workspace_list_channels**](ChannelsApi.md#workspace_list_channels) | **GET** /v1/organizations/{org}/workspaces/{workspace}/channels | 
[**workspace_send_channel_message**](ChannelsApi.md#workspace_send_channel_message) | **POST** /v1/organizations/{org}/workspaces/{workspace}/channels/messages | 



## create_channel

> models::CreateChannelResponse create_channel(create_channel_request)
Create a channel.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_channel_request** | [**CreateChannelRequest**](CreateChannelRequest.md) |  | [required] |

### Return type

[**models::CreateChannelResponse**](CreateChannelResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## execute_channel_action

> models::ExecuteChatActionResponse execute_channel_action(execute_chat_action_request)
Dispatch a channel action by id.

Generic action-execution endpoint. `params` shape varies per `action_id`; consult `GET /v1/channels/actions` for the per-id contract. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**execute_chat_action_request** | [**ExecuteChatActionRequest**](ExecuteChatActionRequest.md) |  | [required] |

### Return type

[**models::ExecuteChatActionResponse**](ExecuteChatActionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## join_channel

> models::SuccessFlag join_channel(id, channel_membership_request)
Join a channel.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Channel id (provider-scoped). | [required] |
**channel_membership_request** | Option<[**ChannelMembershipRequest**](ChannelMembershipRequest.md)> |  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## leave_channel

> models::SuccessFlag leave_channel(id, channel_membership_request)
Leave a channel.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Channel id (provider-scoped). | [required] |
**channel_membership_request** | Option<[**ChannelMembershipRequest**](ChannelMembershipRequest.md)> |  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_channel_actions

> models::ChatActionsList list_channel_actions()
Discover the action catalog for the Channels platform.

Returns the action descriptors the agent layer dispatches via `POST /v1/channels/execute`. Same pattern as the DirectMessages action surface. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ChatActionsList**](ChatActionsList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_channel_messages

> models::ListMessagesResponse list_channel_messages(channel, account_id, account_ids, providers, x_workspace_id, limit, cursor, oldest_first)
List messages in a channel.

Channel ids are provider-scoped; pass `?accountId=` (preferred) or `?accountIds=` to disambiguate when the same id exists on multiple connected accounts (rare). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel** | **String** | Channel id. | [required] |
**account_id** | Option<**String**> |  |  |
**account_ids** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  |  |
**providers** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |
**cursor** | Option<**String**> |  |  |
**oldest_first** | Option<**bool**> |  |  |[default to false]

### Return type

[**models::ListMessagesResponse**](ListMessagesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_channels

> models::ListChannelsResponse list_channels(account_ids, providers, x_workspace_id, limit, cursor, include_archived, types)
List group channels across connected chat providers.

Fan-out list. The Channels surface filters to channel-type conversations only (`type: channel | private`); for direct messages use `/v1/direct-messages`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  |  |
**providers** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |
**cursor** | Option<**String**> | Provider-specific pagination cursor. |  |
**include_archived** | Option<**bool**> |  |  |[default to false]
**types** | Option<[**Vec<String>**](String.md)> | Repeatable filter on `Channel.type`. Defaults applied by the platform exclude DMs; passing this overrides.  |  |

### Return type

[**models::ListChannelsResponse**](ListChannelsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_channel_message

> models::SendChatMessageResponse send_channel_message(send_chat_message_request)
Send a message to a channel.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_chat_message_request** | [**SendChatMessageRequest**](SendChatMessageRequest.md) |  | [required] |

### Return type

[**models::SendChatMessageResponse**](SendChatMessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_create_channel

> std::collections::HashMap<String, serde_json::Value> workspace_create_channel(org, workspace, request_body)


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


## workspace_execute_channel_action

> std::collections::HashMap<String, serde_json::Value> workspace_execute_channel_action(org, workspace, request_body)


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


## workspace_join_channel

> workspace_join_channel(org, workspace, id, request_body)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |
**request_body** | Option<[**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_leave_channel

> workspace_leave_channel(org, workspace, id, request_body)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |
**request_body** | Option<[**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_list_channel_actions

> std::collections::HashMap<String, serde_json::Value> workspace_list_channel_actions(org, workspace)


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


## workspace_list_channel_messages

> std::collections::HashMap<String, serde_json::Value> workspace_list_channel_messages(org, workspace)


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


## workspace_list_channels

> std::collections::HashMap<String, serde_json::Value> workspace_list_channels(org, workspace)


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


## workspace_send_channel_message

> std::collections::HashMap<String, serde_json::Value> workspace_send_channel_message(org, workspace, request_body)


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

