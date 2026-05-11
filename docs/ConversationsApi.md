# \ConversationsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_conversation**](ConversationsApi.md#create_conversation) | **POST** /v1/conversations | Persist a new LLM conversation.
[**delete_conversation**](ConversationsApi.md#delete_conversation) | **DELETE** /v1/conversations/{id} | Soft-delete a conversation.
[**get_conversation**](ConversationsApi.md#get_conversation) | **GET** /v1/conversations/{id} | Fetch one conversation.
[**get_latest_conversation_for_context**](ConversationsApi.md#get_latest_conversation_for_context) | **GET** /v1/conversations/latest | Fetch the most recently active conversation for a given context tag.
[**list_conversation_messages**](ConversationsApi.md#list_conversation_messages) | **GET** /v1/conversations/{id}/messages | List messages in a conversation.
[**list_conversations**](ConversationsApi.md#list_conversations) | **GET** /v1/conversations | List the caller's persisted LLM conversations.
[**save_conversation_message**](ConversationsApi.md#save_conversation_message) | **POST** /v1/conversations/{id}/messages | Append a message to a conversation.
[**update_conversation**](ConversationsApi.md#update_conversation) | **PATCH** /v1/conversations/{id} | Update conversation metadata (title, context, cwd, session_id, pinned).
[**update_conversation_message_metadata**](ConversationsApi.md#update_conversation_message_metadata) | **PATCH** /v1/conversations/{id}/messages | Patch metadata on an existing message. Body must include the message id (path is the conversation id, not the message). 



## create_conversation

> models::Conversation create_conversation(create_conversation_request)
Persist a new LLM conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_conversation_request** | Option<[**CreateConversationRequest**](CreateConversationRequest.md)> |  |  |

### Return type

[**models::Conversation**](Conversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_conversation

> delete_conversation(id)
Soft-delete a conversation.

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


## get_conversation

> models::Conversation get_conversation(id)
Fetch one conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::Conversation**](Conversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_latest_conversation_for_context

> models::Conversation get_latest_conversation_for_context(context)
Fetch the most recently active conversation for a given context tag.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**context** | **String** |  | [required] |

### Return type

[**models::Conversation**](Conversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversation_messages

> Vec<models::ConversationMessage> list_conversation_messages(id, limit, before)
List messages in a conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |
**before** | Option<**String**> |  |  |

### Return type

[**Vec<models::ConversationMessage>**](ConversationMessage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversations

> Vec<models::Conversation> list_conversations(context, limit)
List the caller's persisted LLM conversations.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**context** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |

### Return type

[**Vec<models::Conversation>**](Conversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## save_conversation_message

> models::ConversationMessage save_conversation_message(id, save_message_request)
Append a message to a conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**save_message_request** | [**SaveMessageRequest**](SaveMessageRequest.md) |  | [required] |

### Return type

[**models::ConversationMessage**](ConversationMessage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_conversation

> models::Conversation update_conversation(id, update_conversation_request)
Update conversation metadata (title, context, cwd, session_id, pinned).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_conversation_request** | [**UpdateConversationRequest**](UpdateConversationRequest.md) |  | [required] |

### Return type

[**models::Conversation**](Conversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_conversation_message_metadata

> models::ConversationMessage update_conversation_message_metadata(id, update_message_metadata_request)
Patch metadata on an existing message. Body must include the message id (path is the conversation id, not the message). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_message_metadata_request** | [**UpdateMessageMetadataRequest**](UpdateMessageMetadataRequest.md) |  | [required] |

### Return type

[**models::ConversationMessage**](ConversationMessage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

