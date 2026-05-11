# \NativeDmApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_native_dm_reaction**](NativeDmApi.md#add_native_dm_reaction) | **POST** /v1/native/dm/messages/{messageId}/reactions | Add a reaction to a DM message.
[**attach_to_native_dm_message**](NativeDmApi.md#attach_to_native_dm_message) | **POST** /v1/native/dm/messages/{messageId}/attachments | Attach a file to a DM message.
[**delete_native_dm_message**](NativeDmApi.md#delete_native_dm_message) | **DELETE** /v1/native/dm/{dmId}/messages/{messageId} | Delete a DM message.
[**forward_native_dm_message**](NativeDmApi.md#forward_native_dm_message) | **POST** /v1/native/dm/messages/{messageId}/forward | Forward a DM message to another conversation.
[**list_native_dm_channels**](NativeDmApi.md#list_native_dm_channels) | **GET** /v1/native/dm | List the caller's DM channels.
[**list_native_dm_conversations**](NativeDmApi.md#list_native_dm_conversations) | **GET** /v1/native/dm/conversations | List DM conversations with metadata (last message, unread count, etc.).
[**list_native_dm_messages**](NativeDmApi.md#list_native_dm_messages) | **GET** /v1/native/dm/{dmId}/messages | List messages in a DM.
[**list_native_dm_pinned_messages**](NativeDmApi.md#list_native_dm_pinned_messages) | **GET** /v1/native/dm/{dmId}/pinned | List pinned messages in a DM.
[**list_native_dm_thread_replies**](NativeDmApi.md#list_native_dm_thread_replies) | **GET** /v1/native/dm/{dmId}/messages/{messageId}/replies | List threaded replies on a message.
[**mark_native_dm_read**](NativeDmApi.md#mark_native_dm_read) | **POST** /v1/native/dm/{dmId}/read | Mark a DM as read.
[**mute_native_dm**](NativeDmApi.md#mute_native_dm) | **POST** /v1/native/dm/{dmId}/mute | Mute a DM.
[**pin_native_dm_conversation**](NativeDmApi.md#pin_native_dm_conversation) | **POST** /v1/native/dm/{dmId}/pin | Pin a DM conversation in the sidebar.
[**pin_native_dm_message**](NativeDmApi.md#pin_native_dm_message) | **POST** /v1/native/dm/messages/{messageId}/pin | Pin a DM message.
[**post_native_dm_message**](NativeDmApi.md#post_native_dm_message) | **POST** /v1/native/dm | Post a DM message (top-level entry).
[**post_native_dm_thread_reply**](NativeDmApi.md#post_native_dm_thread_reply) | **POST** /v1/native/dm/{dmId}/messages/{messageId}/replies | Post a threaded reply.
[**remove_native_dm_reaction**](NativeDmApi.md#remove_native_dm_reaction) | **DELETE** /v1/native/dm/messages/{messageId}/reactions/{emoji} | Remove a reaction.
[**search_native_dm_messages**](NativeDmApi.md#search_native_dm_messages) | **GET** /v1/native/dm/search | Search DM messages.
[**set_native_dm_draft**](NativeDmApi.md#set_native_dm_draft) | **PUT** /v1/native/dm/{dmId}/draft | Save a draft on a DM conversation.
[**unpin_native_dm_conversation**](NativeDmApi.md#unpin_native_dm_conversation) | **DELETE** /v1/native/dm/{dmId}/pin | Unpin a DM conversation.
[**unpin_native_dm_message**](NativeDmApi.md#unpin_native_dm_message) | **DELETE** /v1/native/dm/messages/{messageId}/pin | Unpin a DM message.
[**update_native_dm_message**](NativeDmApi.md#update_native_dm_message) | **PATCH** /v1/native/dm/{dmId}/messages/{messageId} | Update a DM message body.



## add_native_dm_reaction

> std::collections::HashMap<String, serde_json::Value> add_native_dm_reaction(message_id, request_body)
Add a reaction to a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## attach_to_native_dm_message

> std::collections::HashMap<String, serde_json::Value> attach_to_native_dm_message(message_id, request_body)
Attach a file to a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_native_dm_message

> delete_native_dm_message(dm_id, message_id)
Delete a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |
**message_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## forward_native_dm_message

> std::collections::HashMap<String, serde_json::Value> forward_native_dm_message(message_id, request_body)
Forward a DM message to another conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_native_dm_channels

> std::collections::HashMap<String, serde_json::Value> list_native_dm_channels()
List the caller's DM channels.

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


## list_native_dm_conversations

> std::collections::HashMap<String, serde_json::Value> list_native_dm_conversations()
List DM conversations with metadata (last message, unread count, etc.).

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


## list_native_dm_messages

> std::collections::HashMap<String, serde_json::Value> list_native_dm_messages(dm_id)
List messages in a DM.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_native_dm_pinned_messages

> std::collections::HashMap<String, serde_json::Value> list_native_dm_pinned_messages(dm_id)
List pinned messages in a DM.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_native_dm_thread_replies

> std::collections::HashMap<String, serde_json::Value> list_native_dm_thread_replies(dm_id, message_id)
List threaded replies on a message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |
**message_id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_native_dm_read

> mark_native_dm_read(dm_id)
Mark a DM as read.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mute_native_dm

> mute_native_dm(dm_id, request_body)
Mute a DM.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |
**request_body** | Option<[**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md)> |  |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pin_native_dm_conversation

> pin_native_dm_conversation(dm_id)
Pin a DM conversation in the sidebar.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pin_native_dm_message

> pin_native_dm_message(message_id)
Pin a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_native_dm_message

> std::collections::HashMap<String, serde_json::Value> post_native_dm_message(request_body)
Post a DM message (top-level entry).

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


## post_native_dm_thread_reply

> std::collections::HashMap<String, serde_json::Value> post_native_dm_thread_reply(dm_id, message_id, request_body)
Post a threaded reply.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |
**message_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_native_dm_reaction

> remove_native_dm_reaction(message_id, emoji)
Remove a reaction.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**emoji** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_native_dm_messages

> std::collections::HashMap<String, serde_json::Value> search_native_dm_messages(q)
Search DM messages.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | Option<**String**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_native_dm_draft

> set_native_dm_draft(dm_id, request_body)
Save a draft on a DM conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unpin_native_dm_conversation

> unpin_native_dm_conversation(dm_id)
Unpin a DM conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unpin_native_dm_message

> unpin_native_dm_message(message_id)
Unpin a DM message.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_native_dm_message

> std::collections::HashMap<String, serde_json::Value> update_native_dm_message(dm_id, message_id, request_body)
Update a DM message body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dm_id** | **String** |  | [required] |
**message_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

