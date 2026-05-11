# \WorkspacesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_workspace_invitation**](WorkspacesApi.md#accept_workspace_invitation) | **POST** /v1/invitations/{token}/accept | Accept a workspace invitation by token. The signed-in user's email must match the invitation. Organization-token accept lives at `POST /v1/organizations/{org}/accept-invitation`. 
[**add_workspace_member**](WorkspacesApi.md#add_workspace_member) | **POST** /v1/workspaces/{workspaceId}/members | Add a member directly (skips invitation flow).
[**create_workspace**](WorkspacesApi.md#create_workspace) | **POST** /v1/workspaces | Create a workspace. Requires `organizationId` in the body — bare \"personal\" workspaces aren't supported on the public API. 
[**create_workspace_invitation**](WorkspacesApi.md#create_workspace_invitation) | **POST** /v1/workspaces/{workspaceId}/invitations | Invite a user to a workspace.
[**get_public_invitation**](WorkspacesApi.md#get_public_invitation) | **GET** /invitations/{token} | Fetch invitation details by token (unauthenticated). Used by the renderer to show invitation context before the user signs in. 
[**get_workspace**](WorkspacesApi.md#get_workspace) | **GET** /v1/workspaces/{workspaceId} | Fetch a single workspace by id.
[**list_my_workspaces**](WorkspacesApi.md#list_my_workspaces) | **GET** /v1/workspaces | List the caller's workspaces (across organizations).
[**list_workspace_invitations**](WorkspacesApi.md#list_workspace_invitations) | **GET** /v1/workspaces/{workspaceId}/invitations | List pending workspace invitations.
[**list_workspace_members**](WorkspacesApi.md#list_workspace_members) | **GET** /v1/workspaces/{workspaceId}/members | List members of a workspace.
[**remove_workspace_member**](WorkspacesApi.md#remove_workspace_member) | **DELETE** /v1/workspaces/{workspaceId}/members/{memberId} | Remove a member from the workspace.
[**revoke_workspace_invitation**](WorkspacesApi.md#revoke_workspace_invitation) | **DELETE** /v1/workspaces/{workspaceId}/invitations/{invitationId} | Revoke a pending workspace invitation.
[**update_workspace**](WorkspacesApi.md#update_workspace) | **PATCH** /v1/workspaces/{workspaceId} | Update workspace metadata.
[**update_workspace_member**](WorkspacesApi.md#update_workspace_member) | **PATCH** /v1/workspaces/{workspaceId}/members/{memberId} | Update a member's role.



## accept_workspace_invitation

> std::collections::HashMap<String, serde_json::Value> accept_workspace_invitation(token)
Accept a workspace invitation by token. The signed-in user's email must match the invitation. Organization-token accept lives at `POST /v1/organizations/{org}/accept-invitation`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_workspace_member

> std::collections::HashMap<String, serde_json::Value> add_workspace_member(workspace_id, add_workspace_member_request)
Add a member directly (skips invitation flow).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**add_workspace_member_request** | [**AddWorkspaceMemberRequest**](AddWorkspaceMemberRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_workspace

> models::WorkspaceEnvelope create_workspace(create_workspace_request)
Create a workspace. Requires `organizationId` in the body — bare \"personal\" workspaces aren't supported on the public API. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_workspace_request** | [**CreateWorkspaceRequest**](CreateWorkspaceRequest.md) |  | [required] |

### Return type

[**models::WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_workspace_invitation

> models::WorkspaceInvitation create_workspace_invitation(workspace_id, create_workspace_invitation_request)
Invite a user to a workspace.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**create_workspace_invitation_request** | [**CreateWorkspaceInvitationRequest**](CreateWorkspaceInvitationRequest.md) |  | [required] |

### Return type

[**models::WorkspaceInvitation**](WorkspaceInvitation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_public_invitation

> models::PublicInvitationPayload get_public_invitation(token)
Fetch invitation details by token (unauthenticated). Used by the renderer to show invitation context before the user signs in. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** |  | [required] |

### Return type

[**models::PublicInvitationPayload**](PublicInvitationPayload.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_workspace

> models::WorkspaceEnvelope get_workspace(workspace_id)
Fetch a single workspace by id.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |

### Return type

[**models::WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_my_workspaces

> models::WorkspaceListResponse list_my_workspaces()
List the caller's workspaces (across organizations).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::WorkspaceListResponse**](WorkspaceListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_workspace_invitations

> models::WorkspaceInvitationListResponse list_workspace_invitations(workspace_id)
List pending workspace invitations.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |

### Return type

[**models::WorkspaceInvitationListResponse**](WorkspaceInvitationListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_workspace_members

> models::WorkspaceMemberListResponse list_workspace_members(workspace_id)
List members of a workspace.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |

### Return type

[**models::WorkspaceMemberListResponse**](WorkspaceMemberListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_workspace_member

> remove_workspace_member(workspace_id, member_id)
Remove a member from the workspace.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**member_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_workspace_invitation

> revoke_workspace_invitation(workspace_id, invitation_id)
Revoke a pending workspace invitation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**invitation_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_workspace

> models::WorkspaceEnvelope update_workspace(workspace_id, update_workspace_request)
Update workspace metadata.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**update_workspace_request** | [**UpdateWorkspaceRequest**](UpdateWorkspaceRequest.md) |  | [required] |

### Return type

[**models::WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_workspace_member

> std::collections::HashMap<String, serde_json::Value> update_workspace_member(workspace_id, member_id, update_workspace_member_request)
Update a member's role.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**member_id** | **String** |  | [required] |
**update_workspace_member_request** | [**UpdateWorkspaceMemberRequest**](UpdateWorkspaceMemberRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

