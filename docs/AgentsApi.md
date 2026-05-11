# \AgentsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_agent**](AgentsApi.md#create_agent) | **POST** /v1/agents | Create a new agent configuration.
[**create_agent_conversation**](AgentsApi.md#create_agent_conversation) | **POST** /v1/agent/conversations | Create a new agent-platform conversation.
[**create_agent_message**](AgentsApi.md#create_agent_message) | **POST** /v1/agent/conversations/{id}/messages | Append a message to an agent conversation.
[**delete_agent**](AgentsApi.md#delete_agent) | **DELETE** /v1/agents/{id} | Delete an agent configuration.
[**execute_agent_action**](AgentsApi.md#execute_agent_action) | **POST** /v1/agent/actions/execute | Execute an action through the agent platform.
[**get_agent**](AgentsApi.md#get_agent) | **GET** /v1/agents/{id} | Fetch one agent configuration.
[**get_agent_conversation**](AgentsApi.md#get_agent_conversation) | **GET** /v1/agent/conversations/{id} | Fetch one agent conversation.
[**get_agent_session_context**](AgentsApi.md#get_agent_session_context) | **GET** /v1/agent/session-context | Identity bundle for the SessionStart hook (user + org + workspace + connected accounts) so the agent doesn't fish on its first turn. 
[**list_agent_conversation_messages**](AgentsApi.md#list_agent_conversation_messages) | **GET** /v1/agent/conversations/{id}/messages | List messages on an agent conversation.
[**list_agent_conversations**](AgentsApi.md#list_agent_conversations) | **GET** /v1/agent/conversations | List the caller's agent-platform conversations. Distinct from `/v1/conversations` (renderer-driven sidebar persistence). 
[**list_agents**](AgentsApi.md#list_agents) | **GET** /v1/agents | List the caller's agent configurations.
[**list_preconfigured_agents**](AgentsApi.md#list_preconfigured_agents) | **GET** /v1/agents/preconfigured | Curated featured agents (e.g. \"Claude Code\", \"Research Assistant\"). Read-only — these are surfaced by the renderer's preconfigured-picker UI. 
[**update_agent**](AgentsApi.md#update_agent) | **PATCH** /v1/agents/{id} | Update an agent configuration.



## create_agent

> models::Agent create_agent(create_agent_request)
Create a new agent configuration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_agent_request** | [**CreateAgentRequest**](CreateAgentRequest.md) |  | [required] |

### Return type

[**models::Agent**](Agent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_agent_conversation

> models::AgentConversation create_agent_conversation(create_agent_conversation_request)
Create a new agent-platform conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_agent_conversation_request** | Option<[**CreateAgentConversationRequest**](CreateAgentConversationRequest.md)> |  |  |

### Return type

[**models::AgentConversation**](AgentConversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_agent_message

> models::AgentMessage create_agent_message(id, create_agent_message_request)
Append a message to an agent conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**create_agent_message_request** | [**CreateAgentMessageRequest**](CreateAgentMessageRequest.md) |  | [required] |

### Return type

[**models::AgentMessage**](AgentMessage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_agent

> delete_agent(id)
Delete an agent configuration.

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


## execute_agent_action

> models::ExecuteActionResponse execute_agent_action(execute_action_request)
Execute an action through the agent platform.

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


## get_agent

> models::Agent get_agent(id)
Fetch one agent configuration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::Agent**](Agent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_agent_conversation

> models::AgentConversation get_agent_conversation(id)
Fetch one agent conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::AgentConversation**](AgentConversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_agent_session_context

> models::AgentSessionContext get_agent_session_context()
Identity bundle for the SessionStart hook (user + org + workspace + connected accounts) so the agent doesn't fish on its first turn. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AgentSessionContext**](AgentSessionContext.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_agent_conversation_messages

> models::AgentMessageListResponse list_agent_conversation_messages(id)
List messages on an agent conversation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::AgentMessageListResponse**](AgentMessageListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_agent_conversations

> models::AgentConversationListResponse list_agent_conversations()
List the caller's agent-platform conversations. Distinct from `/v1/conversations` (renderer-driven sidebar persistence). 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AgentConversationListResponse**](AgentConversationListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_agents

> models::AgentListResponse list_agents()
List the caller's agent configurations.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::AgentListResponse**](AgentListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_preconfigured_agents

> Vec<models::PreconfiguredAgent> list_preconfigured_agents()
Curated featured agents (e.g. \"Claude Code\", \"Research Assistant\"). Read-only — these are surfaced by the renderer's preconfigured-picker UI. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**Vec<models::PreconfiguredAgent>**](PreconfiguredAgent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_agent

> models::Agent update_agent(id, update_agent_request)
Update an agent configuration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_agent_request** | [**UpdateAgentRequest**](UpdateAgentRequest.md) |  | [required] |

### Return type

[**models::Agent**](Agent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

