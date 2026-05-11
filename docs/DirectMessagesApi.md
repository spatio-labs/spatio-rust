# \DirectMessagesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_dm_reaction**](DirectMessagesApi.md#add_dm_reaction) | **POST** /v1/direct-messages/messages/{messageId}/reactions | React to a DM message.
[**attach_to_dm_message**](DirectMessagesApi.md#attach_to_dm_message) | **POST** /v1/direct-messages/messages/{messageId}/attachments | Attach a file/image/etc. to an existing DM message.
[**execute_dm_action**](DirectMessagesApi.md#execute_dm_action) | **POST** /v1/direct-messages/execute | Dispatch a DM action by id.
[**forward_dm_message**](DirectMessagesApi.md#forward_dm_message) | **POST** /v1/direct-messages/messages/{messageId}/forward | Forward a DM message to another DM or channel.
[**get_dm_user**](DirectMessagesApi.md#get_dm_user) | **GET** /v1/direct-messages/users/{id} | Fetch one chat user.
[**list_direct_conversations_enriched**](DirectMessagesApi.md#list_direct_conversations_enriched) | **GET** /v1/direct-messages/conversations | Enriched DM conversation list with unread + pin + draft state.
[**list_direct_message_conversations**](DirectMessagesApi.md#list_direct_message_conversations) | **GET** /v1/direct-messages | List 1:1 and group DM conversations.
[**list_direct_messages**](DirectMessagesApi.md#list_direct_messages) | **GET** /v1/direct-messages/messages | List messages in a DM conversation.
[**list_dm_actions**](DirectMessagesApi.md#list_dm_actions) | **GET** /v1/direct-messages/actions | Discover the action catalog for DirectMessages.
[**list_dm_pinned_messages**](DirectMessagesApi.md#list_dm_pinned_messages) | **GET** /v1/direct-messages/{dmId}/pinned | List pinned messages in a DM conversation.
[**list_dm_thread_replies**](DirectMessagesApi.md#list_dm_thread_replies) | **GET** /v1/direct-messages/{dmId}/messages/{messageId}/replies | List replies in a DM message thread.
[**list_dm_users**](DirectMessagesApi.md#list_dm_users) | **GET** /v1/direct-messages/users | List chat users (DM contacts) across connected accounts.
[**mark_dm_read**](DirectMessagesApi.md#mark_dm_read) | **POST** /v1/direct-messages/{dmId}/read | Mark a DM message read.
[**mute_dm**](DirectMessagesApi.md#mute_dm) | **POST** /v1/direct-messages/{dmId}/mute | Mute a DM conversation (until a time, or forever).
[**pin_dm_conversation**](DirectMessagesApi.md#pin_dm_conversation) | **POST** /v1/direct-messages/{dmId}/pin | Pin a DM conversation to the top of the sidebar.
[**pin_dm_message**](DirectMessagesApi.md#pin_dm_message) | **POST** /v1/direct-messages/messages/{messageId}/pin | Pin a DM message.
[**post_dm_thread_reply**](DirectMessagesApi.md#post_dm_thread_reply) | **POST** /v1/direct-messages/{dmId}/messages/{messageId}/replies | Reply in a DM message thread.
[**remove_dm_reaction**](DirectMessagesApi.md#remove_dm_reaction) | **DELETE** /v1/direct-messages/messages/{messageId}/reactions/{emoji} | Remove a DM message reaction.
[**search_direct_messages**](DirectMessagesApi.md#search_direct_messages) | **GET** /v1/direct-messages/search | Search across DM messages.
[**send_direct_message**](DirectMessagesApi.md#send_direct_message) | **POST** /v1/direct-messages/messages | Send a DM.
[**set_dm_draft**](DirectMessagesApi.md#set_dm_draft) | **PUT** /v1/direct-messages/{dmId}/draft | Save the unsent draft text for a DM.
[**unpin_dm_conversation**](DirectMessagesApi.md#unpin_dm_conversation) | **DELETE** /v1/direct-messages/{dmId}/pin | Unpin a DM conversation.
[**unpin_dm_message**](DirectMessagesApi.md#unpin_dm_message) | **DELETE** /v1/direct-messages/messages/{messageId}/pin | Unpin a DM message.
[**workspace_execute_dm_action**](DirectMessagesApi.md#workspace_execute_dm_action) | **POST** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/execute | 
[**workspace_get_dm_user**](DirectMessagesApi.md#workspace_get_dm_user) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/users/{id} | 
[**workspace_list_direct_messages**](DirectMessagesApi.md#workspace_list_direct_messages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages | 
[**workspace_list_dm_actions**](DirectMessagesApi.md#workspace_list_dm_actions) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/actions | 
[**workspace_list_dm_conversations**](DirectMessagesApi.md#workspace_list_dm_conversations) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/conversations | 
[**workspace_list_dm_messages**](DirectMessagesApi.md#workspace_list_dm_messages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/messages | 
[**workspace_list_dm_users**](DirectMessagesApi.md#workspace_list_dm_users) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/users | 
[**workspace_send_direct_message**](DirectMessagesApi.md#workspace_send_direct_message) | **POST** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/messages | 



## add_dm_reaction

> models::DmReactionResponse add_dm_reaction(message_id, dm_reaction_request)
React to a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** | Chat-message id. | [required] |
**dm_reaction_request** | [**DmReactionRequest**](DmReactionRequest.md) |  | [required] |

### Return type

[**models::DmReactionResponse**](DMReactionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## attach_to_dm_message

> models::DmMessageEnvelope attach_to_dm_message(message_id, dm_attach_request)
Attach a file/image/etc. to an existing DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** | Chat-message id. | [required] |
**dm_attach_request** | [**DmAttachRequest**](DmAttachRequest.md) |  | [required] |

### Return type

[**models::DmMessageEnvelope**](DMMessageEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## execute_dm_action

> models::ExecuteChatActionResponse execute_dm_action(execute_chat_action_request)
Dispatch a DM action by id.

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


## forward_dm_message

> models::DmMessageEnvelope forward_dm_message(message_id, dm_forward_request)
Forward a DM message to another DM or channel.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** | Chat-message id. | [required] |
**dm_forward_request** | [**DmForwardRequest**](DmForwardRequest.md) |  | [required] |

### Return type

[**models::DmMessageEnvelope**](DMMessageEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_dm_user

> models::GetChatUserResponse get_dm_user(id, account_id)
Fetch one chat user.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Chat-user id (provider-scoped). | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::GetChatUserResponse**](GetChatUserResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_direct_conversations_enriched

> std::collections::HashMap<String, serde_json::Value> list_direct_conversations_enriched(account_id, x_workspace_id)
Enriched DM conversation list with unread + pin + draft state.

Native fast-path. Returns conversations augmented with the DM-feature state (unread counts, pinned/muted flags, saved drafts) the renderer's DM UI consumes. The shape is provider-specific and treated as opaque. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_direct_message_conversations

> models::ListChannelsResponse list_direct_message_conversations(account_ids, providers, x_workspace_id, limit, cursor, include_archived)
List 1:1 and group DM conversations.

Returns DM-type conversations only (`type: im | mpim`). Channel-type conversations are surfaced via `/v1/channels`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  |  |
**providers** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |
**cursor** | Option<**String**> |  |  |
**include_archived** | Option<**bool**> |  |  |[default to false]

### Return type

[**models::ListChannelsResponse**](ListChannelsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_direct_messages

> models::ListMessagesResponse list_direct_messages(channel, account_id, account_ids, providers, x_workspace_id, limit, cursor, oldest_first)
List messages in a DM conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**channel** | **String** | DM conversation id. | [required] |
**account_id** | Option<**String**> |  |  |
**account_ids** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  |  |
**providers** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |
**cursor** | Option<**String**> |  |  |
**oldest_first** | Option<**bool**> |  |  |

### Return type

[**models::ListMessagesResponse**](ListMessagesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_dm_actions

> models::ChatActionsList list_dm_actions()
Discover the action catalog for DirectMessages.

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


## list_dm_pinned_messages

> models::DmPinnedList list_dm_pinned_messages(dm_id, account_id)
List pinned messages in a DM conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::DmPinnedList**](DMPinnedList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_dm_thread_replies

> std::collections::HashMap<String, serde_json::Value> list_dm_thread_replies(dm_id, message_id, account_id)
List replies in a DM message thread.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**message_id** | **String** | Chat-message id. | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_dm_users

> models::ListChatUsersResponse list_dm_users(account_ids, providers, x_workspace_id, limit, cursor)
List chat users (DM contacts) across connected accounts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_ids** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  |  |
**providers** | Option<[**Vec<String>**](String.md)> | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |
**cursor** | Option<**String**> |  |  |

### Return type

[**models::ListChatUsersResponse**](ListChatUsersResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_dm_read

> models::SuccessFlag mark_dm_read(dm_id, dm_mark_read_request)
Mark a DM message read.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**dm_mark_read_request** | [**DmMarkReadRequest**](DmMarkReadRequest.md) |  | [required] |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mute_dm

> models::DmMuteResponse mute_dm(dm_id, dm_mute_request)
Mute a DM conversation (until a time, or forever).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**dm_mute_request** | [**DmMuteRequest**](DmMuteRequest.md) |  | [required] |

### Return type

[**models::DmMuteResponse**](DMMuteResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pin_dm_conversation

> models::SuccessFlag pin_dm_conversation(dm_id, account_id)
Pin a DM conversation to the top of the sidebar.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pin_dm_message

> models::SuccessFlag pin_dm_message(message_id, channel_membership_request)
Pin a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** | Chat-message id. | [required] |
**channel_membership_request** | Option<[**ChannelMembershipRequest**](ChannelMembershipRequest.md)> |  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_dm_thread_reply

> models::DmMessageEnvelope post_dm_thread_reply(dm_id, message_id, dm_thread_reply_request, account_id)
Reply in a DM message thread.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**message_id** | **String** | Chat-message id. | [required] |
**dm_thread_reply_request** | [**DmThreadReplyRequest**](DmThreadReplyRequest.md) |  | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::DmMessageEnvelope**](DMMessageEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_dm_reaction

> models::DmReactionResponse remove_dm_reaction(message_id, emoji, account_id)
Remove a DM message reaction.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** | Chat-message id. | [required] |
**emoji** | **String** | Reaction emoji (e.g. `+1`, `eyes`, `pepper`). | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::DmReactionResponse**](DMReactionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_direct_messages

> models::DmSearchResults search_direct_messages(q, limit, dm_id, user, account_id)
Search across DM messages.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Free-form query string. | [required] |
**limit** | Option<**i32**> |  |  |
**dm_id** | Option<**String**> | Restrict to one conversation. |  |
**user** | Option<**String**> | Restrict to messages from this user id. |  |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::DmSearchResults**](DMSearchResults.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_direct_message

> models::SendChatMessageResponse send_direct_message(send_chat_message_request)
Send a DM.

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


## set_dm_draft

> models::SuccessFlag set_dm_draft(dm_id, dm_set_draft_request)
Save the unsent draft text for a DM.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**dm_set_draft_request** | [**DmSetDraftRequest**](DmSetDraftRequest.md) |  | [required] |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unpin_dm_conversation

> models::SuccessFlag unpin_dm_conversation(dm_id, account_id)
Unpin a DM conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** | Direct-message conversation id. | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unpin_dm_message

> models::SuccessFlag unpin_dm_message(message_id, account_id)
Unpin a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** | Chat-message id. | [required] |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_execute_dm_action

> std::collections::HashMap<String, serde_json::Value> workspace_execute_dm_action(org, workspace, request_body)


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


## workspace_get_dm_user

> std::collections::HashMap<String, serde_json::Value> workspace_get_dm_user(org, workspace, id)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_list_direct_messages

> std::collections::HashMap<String, serde_json::Value> workspace_list_direct_messages(org, workspace)


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


## workspace_list_dm_actions

> std::collections::HashMap<String, serde_json::Value> workspace_list_dm_actions(org, workspace)


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


## workspace_list_dm_conversations

> std::collections::HashMap<String, serde_json::Value> workspace_list_dm_conversations(org, workspace)


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


## workspace_list_dm_messages

> std::collections::HashMap<String, serde_json::Value> workspace_list_dm_messages(org, workspace)


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


## workspace_list_dm_users

> std::collections::HashMap<String, serde_json::Value> workspace_list_dm_users(org, workspace)


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


## workspace_send_direct_message

> std::collections::HashMap<String, serde_json::Value> workspace_send_direct_message(org, workspace, request_body)


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

