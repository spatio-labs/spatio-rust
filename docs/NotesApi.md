# \NotesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_block**](NotesApi.md#create_block) | **POST** /v1/notes/{id}/blocks | Insert a block in a note.
[**create_note**](NotesApi.md#create_note) | **POST** /v1/notes | Create a note.
[**create_note_comment**](NotesApi.md#create_note_comment) | **POST** /v1/notes/{id}/comments | Create a comment or reply.
[**delete_block**](NotesApi.md#delete_block) | **DELETE** /v1/notes/blocks/{id} | Delete a block.
[**delete_note**](NotesApi.md#delete_note) | **DELETE** /v1/notes/{id} | Delete a note.
[**delete_note_comment**](NotesApi.md#delete_note_comment) | **DELETE** /v1/notes/{id}/comments/{commentId} | Soft-delete (native) or hard-delete (provider) a comment.
[**disable_note_share**](NotesApi.md#disable_note_share) | **DELETE** /v1/notes/{id}/share | Disable public sharing.
[**enable_note_share**](NotesApi.md#enable_note_share) | **POST** /v1/notes/{id}/share | Enable (or update password on) public sharing.
[**get_block**](NotesApi.md#get_block) | **GET** /v1/notes/blocks/{id} | Fetch one block.
[**get_note**](NotesApi.md#get_note) | **GET** /v1/notes/{id} | Fetch one note.
[**get_note_comment**](NotesApi.md#get_note_comment) | **GET** /v1/notes/{id}/comments/{commentId} | Fetch one comment.
[**get_note_share_settings**](NotesApi.md#get_note_share_settings) | **GET** /v1/notes/{id}/share | Fetch share settings for a note.
[**get_public_note**](NotesApi.md#get_public_note) | **GET** /public/notes/{token} | Fetch a publicly shared note.
[**list_blocks**](NotesApi.md#list_blocks) | **GET** /v1/notes/{id}/blocks | List blocks under a note.
[**list_note_comments**](NotesApi.md#list_note_comments) | **GET** /v1/notes/{id}/comments | List comments on a note.
[**list_notes**](NotesApi.md#list_notes) | **GET** /v1/notes | List notes across connected accounts.
[**move_block**](NotesApi.md#move_block) | **POST** /v1/notes/blocks/{id}/move | Reparent or reorder a block.
[**rotate_note_share_token**](NotesApi.md#rotate_note_share_token) | **POST** /v1/notes/{id}/share/rotate | Rotate the share token, invalidating any outstanding URLs.
[**update_block**](NotesApi.md#update_block) | **PATCH** /v1/notes/blocks/{id} | Update a block (partial).
[**update_note**](NotesApi.md#update_note) | **PATCH** /v1/notes/{id} | Update a note (partial).
[**update_note_comment**](NotesApi.md#update_note_comment) | **PATCH** /v1/notes/{id}/comments/{commentId} | Edit a comment.
[**workspace_create_note**](NotesApi.md#workspace_create_note) | **POST** /v1/organizations/{org}/workspaces/{workspace}/notes | 
[**workspace_create_note_block**](NotesApi.md#workspace_create_note_block) | **POST** /v1/organizations/{org}/workspaces/{workspace}/notes/{id}/blocks | 
[**workspace_delete_note**](NotesApi.md#workspace_delete_note) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/notes/{id} | 
[**workspace_delete_note_block**](NotesApi.md#workspace_delete_note_block) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id} | 
[**workspace_get_note**](NotesApi.md#workspace_get_note) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes/{id} | 
[**workspace_get_note_block**](NotesApi.md#workspace_get_note_block) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id} | 
[**workspace_list_note_blocks**](NotesApi.md#workspace_list_note_blocks) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes/{id}/blocks | 
[**workspace_list_notes**](NotesApi.md#workspace_list_notes) | **GET** /v1/organizations/{org}/workspaces/{workspace}/notes | 
[**workspace_move_note_block**](NotesApi.md#workspace_move_note_block) | **POST** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id}/move | 
[**workspace_update_note**](NotesApi.md#workspace_update_note) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/notes/{id} | 
[**workspace_update_note_block**](NotesApi.md#workspace_update_note_block) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/notes/blocks/{id} | 



## create_block

> models::Block create_block(id, create_block_request, account_id, x_workspace_id)
Insert a block in a note.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**create_block_request** | [**CreateBlockRequest**](CreateBlockRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Block**](Block.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_note

> models::Note create_note(create_note_request, account_id, provider, x_workspace_id)
Create a note.

Creates a new note under the target account. The target is resolved in this order: `accountId` field on the body → `?accountId=` query → `provider` field on the body → `?provider=` query → the caller's single connected account (errors with `ambiguous_account` if more than one is connected and no selector is supplied). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_note_request** | [**CreateNoteRequest**](CreateNoteRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Note**](Note.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_note_comment

> models::CommentMutationResponse create_note_comment(id, create_comment_request, account_id, x_workspace_id)
Create a comment or reply.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**create_comment_request** | [**CreateCommentRequest**](CreateCommentRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::CommentMutationResponse**](CommentMutationResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_block

> models::SuccessFlag delete_block(id, account_id, x_workspace_id)
Delete a block.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Block id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_note

> models::SuccessFlag delete_note(id, account_id, x_workspace_id)
Delete a note.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_note_comment

> models::SuccessFlag delete_note_comment(id, comment_id, account_id, x_workspace_id)
Soft-delete (native) or hard-delete (provider) a comment.

Allowed for the comment author and for the note owner. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**comment_id** | **String** | Comment id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## disable_note_share

> disable_note_share(id, account_id, x_workspace_id)
Disable public sharing.

Owner-only. Subsequent public viewer requests 404.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_note_share

> models::ShareSettings enable_note_share(id, account_id, x_workspace_id, enable_share_request)
Enable (or update password on) public sharing.

Owner-only. Calling with an empty body or `setPassword: false` flips the note public without changing the password. With `setPassword: true`, applies `password` (empty string clears). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**enable_share_request** | Option<[**EnableShareRequest**](EnableShareRequest.md)> |  |  |

### Return type

[**models::ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_block

> models::Block get_block(id, account_id, x_workspace_id)
Fetch one block.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Block id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Block**](Block.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_note

> models::Note get_note(id, account_id, x_workspace_id)
Fetch one note.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Note**](Note.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_note_comment

> models::CommentResponse get_note_comment(id, comment_id, account_id, x_workspace_id)
Fetch one comment.

Useful for permalink hydration when the renderer deep-links into a reply thread. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**comment_id** | **String** | Comment id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::CommentResponse**](CommentResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_note_share_settings

> models::ShareSettings get_note_share_settings(id, account_id, x_workspace_id)
Fetch share settings for a note.

Owner-only. Returns the current public-share configuration, including the share token and computed public viewer URL when the note is currently public. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_public_note

> std::collections::HashMap<String, serde_json::Value> get_public_note(token, password)
Fetch a publicly shared note.

Unauthenticated. The share token is the credential. For password-protected notes the password is supplied via the `?password=` query param; the response distinguishes \"no password supplied\" from \"wrong password\" so the viewer can render the right prompt.  Unknown tokens and disabled-share notes both return `404` to prevent token enumeration. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | Opaque public-share token. | [required] |
**password** | Option<**String**> | Optional viewer password. |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_blocks

> models::BlockListResponse list_blocks(id, account_id, x_workspace_id, parent_id, limit, offset)
List blocks under a note.

Returns the block tree for a note, paginated. Block listing always targets a single account (the one that owns the note) so it does not fan out — the response is a plain `{ blocks, total }`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**parent_id** | Option<**String**> | Filter to children of this block id. Omit to list root-level blocks.  |  |
**limit** | Option<**i32**> |  |  |[default to 100]
**offset** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::BlockListResponse**](BlockListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_note_comments

> models::CommentListResponse list_note_comments(id, account_id, x_workspace_id)
List comments on a note.

Returns active (non-deleted) comments. When `?accountId=` targets an external provider that supports comments (e.g. Notion), the provider is queried directly; otherwise the native store is used. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::CommentListResponse**](CommentListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_notes

> models::NoteListEnvelope list_notes(account_id, provider, x_workspace_id, archived, parent_id, tags, limit, offset, sort_by, sort_order)
List notes across connected accounts.

Fan-out list. Returns every note visible to the caller across every connected notes provider, paginated by `limit` / `offset`. Pass `?accountId=` or `?provider=` to scope to a single source. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**archived** | Option<**bool**> | When `true`, return archived notes instead of active ones. |  |[default to false]
**parent_id** | Option<**String**> | Filter to notes nested under this parent note id. |  |
**tags** | Option<[**Vec<String>**](String.md)> | Repeatable. Filter to notes carrying every tag listed. |  |
**limit** | Option<**i32**> | Max items to return. Defaults to 50. |  |[default to 50]
**offset** | Option<**i32**> | Number of items to skip. |  |[default to 0]
**sort_by** | Option<**String**> | Sort field. Provider-dependent; the native provider supports `updated_at`, `created_at`, `title`.  |  |[default to updated_at]
**sort_order** | Option<**String**> |  |  |[default to desc]

### Return type

[**models::NoteListEnvelope**](NoteListEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## move_block

> models::SuccessFlag move_block(id, move_block_request, account_id, x_workspace_id)
Reparent or reorder a block.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Block id. | [required] |
**move_block_request** | [**MoveBlockRequest**](MoveBlockRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rotate_note_share_token

> models::ShareSettings rotate_note_share_token(id, account_id, x_workspace_id)
Rotate the share token, invalidating any outstanding URLs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_block

> models::Block update_block(id, update_block_request, account_id, x_workspace_id)
Update a block (partial).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Block id. | [required] |
**update_block_request** | [**UpdateBlockRequest**](UpdateBlockRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Block**](Block.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_note

> models::Note update_note(id, update_note_request, account_id, x_workspace_id)
Update a note (partial).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**update_note_request** | [**UpdateNoteRequest**](UpdateNoteRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Note**](Note.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_note_comment

> models::CommentMutationResponse update_note_comment(id, comment_id, update_comment_request, account_id, x_workspace_id)
Edit a comment.

Only the comment author can edit. The note owner can delete via `DELETE` but cannot rewrite. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Note id. | [required] |
**comment_id** | **String** | Comment id. | [required] |
**update_comment_request** | [**UpdateCommentRequest**](UpdateCommentRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::CommentMutationResponse**](CommentMutationResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_create_note

> std::collections::HashMap<String, serde_json::Value> workspace_create_note(org, workspace, request_body)


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


## workspace_create_note_block

> std::collections::HashMap<String, serde_json::Value> workspace_create_note_block(org, workspace, id, request_body)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
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


## workspace_delete_note

> workspace_delete_note(org, workspace, id)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_delete_note_block

> workspace_delete_note_block(org, workspace, id)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_get_note

> std::collections::HashMap<String, serde_json::Value> workspace_get_note(org, workspace, id)


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


## workspace_get_note_block

> std::collections::HashMap<String, serde_json::Value> workspace_get_note_block(org, workspace, id)


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


## workspace_list_note_blocks

> std::collections::HashMap<String, serde_json::Value> workspace_list_note_blocks(org, workspace, id)


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


## workspace_list_notes

> std::collections::HashMap<String, serde_json::Value> workspace_list_notes(org, workspace)


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


## workspace_move_note_block

> std::collections::HashMap<String, serde_json::Value> workspace_move_note_block(org, workspace, id, request_body)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
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


## workspace_update_note

> std::collections::HashMap<String, serde_json::Value> workspace_update_note(org, workspace, id, request_body)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
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


## workspace_update_note_block

> std::collections::HashMap<String, serde_json::Value> workspace_update_note_block(org, workspace, id, request_body)


### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
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

