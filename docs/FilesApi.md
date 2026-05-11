# \FilesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_delete_files**](FilesApi.md#bulk_delete_files) | **POST** /v1/files/delete | Delete multiple files in one call.
[**bulk_move_files**](FilesApi.md#bulk_move_files) | **POST** /v1/files/move | Move multiple files to a target folder.
[**commit_chunked_upload**](FilesApi.md#commit_chunked_upload) | **POST** /v1/files/upload/chunked/commit | Finalize a chunked-upload session and create the file row.
[**create_file_folder**](FilesApi.md#create_file_folder) | **POST** /v1/files/folders | Create a folder.
[**delete_file**](FilesApi.md#delete_file) | **DELETE** /v1/files/{id} | Delete a file.
[**extract_file_text**](FilesApi.md#extract_file_text) | **GET** /v1/files/{id}/extract-text | Extract text content from a PDF (or other supported file).
[**get_chunked_file_manifest**](FilesApi.md#get_chunked_file_manifest) | **GET** /v1/files/{id}/manifest | Fetch the block manifest for a chunked-uploaded file.
[**get_file**](FilesApi.md#get_file) | **GET** /v1/files/{id} | Fetch one file's metadata.
[**get_file_download_url**](FilesApi.md#get_file_download_url) | **GET** /v1/files/{id}/download | Mint a fresh signed download URL.
[**init_chunked_upload**](FilesApi.md#init_chunked_upload) | **POST** /v1/files/upload/chunked/init | Begin a content-addressed chunked upload session.
[**list_file_folders**](FilesApi.md#list_file_folders) | **GET** /v1/files/folders | List folders across connected file providers.
[**list_files**](FilesApi.md#list_files) | **GET** /v1/files | List files across connected file providers.
[**list_files_and_folders**](FilesApi.md#list_files_and_folders) | **GET** /v1/files/list | Aggregate list of files + folders for renderer file-browser views.
[**move_file**](FilesApi.md#move_file) | **POST** /v1/files/{id}/move | Move a single file to a target folder.
[**search_files**](FilesApi.md#search_files) | **GET** /v1/files/search | Substring-match search across the caller's files.
[**update_file**](FilesApi.md#update_file) | **PATCH** /v1/files/{id} | Update a file's metadata (name, folder, custom fields).
[**upload_chunked_block**](FilesApi.md#upload_chunked_block) | **POST** /v1/files/upload/chunked/blocks | Upload one block for an open chunked-upload session.
[**upload_file**](FilesApi.md#upload_file) | **POST** /v1/files/upload | Upload a file via multipart form.
[**upload_file_base64**](FilesApi.md#upload_file_base64) | **POST** /v1/files/upload/base64 | Upload a file via JSON with base64-encoded content.
[**workspace_commit_chunked_upload**](FilesApi.md#workspace_commit_chunked_upload) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/commit | Workspace-scoped chunked-upload commit (RBAC-protected).
[**workspace_create_file_folder**](FilesApi.md#workspace_create_file_folder) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/folders | Workspace-scoped create-folder (RBAC-protected).
[**workspace_delete_file**](FilesApi.md#workspace_delete_file) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped delete-file.
[**workspace_get_file**](FilesApi.md#workspace_get_file) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped get-file.
[**workspace_get_file_download**](FilesApi.md#workspace_get_file_download) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/download | Workspace-scoped signed-download URL.
[**workspace_get_file_manifest**](FilesApi.md#workspace_get_file_manifest) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/manifest | Workspace-scoped chunked-file manifest.
[**workspace_init_chunked_upload**](FilesApi.md#workspace_init_chunked_upload) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/init | Workspace-scoped chunked-upload init (RBAC-protected).
[**workspace_list_file_folders**](FilesApi.md#workspace_list_file_folders) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/folders | Workspace-scoped list-folders (RBAC-protected).
[**workspace_list_files**](FilesApi.md#workspace_list_files) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files | Workspace-scoped list-files (RBAC-protected).
[**workspace_move_file**](FilesApi.md#workspace_move_file) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/move | Workspace-scoped move-file.
[**workspace_update_file**](FilesApi.md#workspace_update_file) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped update-file.
[**workspace_upload_chunked_block**](FilesApi.md#workspace_upload_chunked_block) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/blocks | Workspace-scoped chunked-upload block (RBAC-protected).
[**workspace_upload_file**](FilesApi.md#workspace_upload_file) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload | Workspace-scoped multipart upload (RBAC-protected).
[**workspace_upload_file_base64**](FilesApi.md#workspace_upload_file_base64) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/base64 | Workspace-scoped base64 upload (RBAC-protected).



## bulk_delete_files

> models::BulkFilesResponse bulk_delete_files(bulk_delete_files_request)
Delete multiple files in one call.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bulk_delete_files_request** | [**BulkDeleteFilesRequest**](BulkDeleteFilesRequest.md) |  | [required] |

### Return type

[**models::BulkFilesResponse**](BulkFilesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## bulk_move_files

> models::BulkFilesResponse bulk_move_files(bulk_move_files_request)
Move multiple files to a target folder.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bulk_move_files_request** | [**BulkMoveFilesRequest**](BulkMoveFilesRequest.md) |  | [required] |

### Return type

[**models::BulkFilesResponse**](BulkFilesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## commit_chunked_upload

> models::CommitChunkedUploadResponse commit_chunked_upload(commit_chunked_upload_request)
Finalize a chunked-upload session and create the file row.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**commit_chunked_upload_request** | [**CommitChunkedUploadRequest**](CommitChunkedUploadRequest.md) |  | [required] |

### Return type

[**models::CommitChunkedUploadResponse**](CommitChunkedUploadResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_file_folder

> models::Folder create_file_folder(create_folder_request, account_id, provider, x_workspace_id)
Create a folder.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_folder_request** | [**CreateFolderRequest**](CreateFolderRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Folder**](Folder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_file

> delete_file(id, account_id, x_workspace_id)
Delete a file.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | File id. | [required] |
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


## extract_file_text

> models::ExtractTextResult extract_file_text(id, account_id, x_workspace_id, page_start, page_end, max_chars)
Extract text content from a PDF (or other supported file).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | File id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**page_start** | Option<**i32**> |  |  |
**page_end** | Option<**i32**> |  |  |
**max_chars** | Option<**i32**> | Truncation limit; sets `truncated: true` when hit. |  |

### Return type

[**models::ExtractTextResult**](ExtractTextResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_chunked_file_manifest

> models::ChunkedFileManifest get_chunked_file_manifest(id, account_id, x_workspace_id)
Fetch the block manifest for a chunked-uploaded file.

Only meaningful for files uploaded via `upload/chunked/_*`. Files uploaded via `upload` or `upload/base64` return `404`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | File id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::ChunkedFileManifest**](ChunkedFileManifest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_file

> models::SpatioFile get_file(id, account_id, x_workspace_id)
Fetch one file's metadata.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | File id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_file_download_url

> models::DownloadFileResponse get_file_download_url(id, account_id, x_workspace_id)
Mint a fresh signed download URL.

Returns a JSON envelope with a pre-signed URL pointing at the backing storage. Clients follow the URL — the platform does not stream bytes through itself. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | File id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::DownloadFileResponse**](DownloadFileResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## init_chunked_upload

> models::InitChunkedUploadResponse init_chunked_upload(init_chunked_upload_request)
Begin a content-addressed chunked upload session.

Client computes per-block hashes ahead of time and submits the list. The server replies with which blocks need uploading vs. already-on-server (deduplicated). Subsequent calls upload the missing blocks via `uploadChunkedBlock`, then `commit`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**init_chunked_upload_request** | [**InitChunkedUploadRequest**](InitChunkedUploadRequest.md) |  | [required] |

### Return type

[**models::InitChunkedUploadResponse**](InitChunkedUploadResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_file_folders

> models::FolderListEnvelope list_file_folders(account_id, provider, x_workspace_id, parent_id, workspace_id, organization_id, limit, offset)
List folders across connected file providers.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**parent_id** | Option<**String**> | Filter to children of this folder. Omit for root. |  |
**workspace_id** | Option<**String**> |  |  |
**organization_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**offset** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::FolderListEnvelope**](FolderListEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_files

> models::FileListEnvelope list_files(account_id, provider, x_workspace_id, folder_id, workspace_id, organization_id, limit, offset, sort_by, sort_order)
List files across connected file providers.

Fan-out list. Returns files from every connected file provider unless filtered by `?accountId=` or `?provider=`. Folder contents are scoped via `?folderId=`; omit for account root. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**folder_id** | Option<**String**> | Filter to one folder. Omit for the account root. |  |
**workspace_id** | Option<**String**> |  |  |
**organization_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**offset** | Option<**i32**> |  |  |[default to 0]
**sort_by** | Option<**String**> | Provider-dependent. Common values: `created_at`, `name`, `size`. |  |[default to created_at]
**sort_order** | Option<**String**> |  |  |[default to DESC]

### Return type

[**models::FileListEnvelope**](FileListEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_files_and_folders

> models::FilesAndFoldersResponse list_files_and_folders(account_id, provider, folder_id, workspace_id, organization_id, limit, offset, sort_by, sort_order)
Aggregate list of files + folders for renderer file-browser views.

Calls `listFiles` and `listFileFolders` in parallel and merges the results. Saves a round-trip when the UI shows both side-by-side. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**folder_id** | Option<**String**> | Filter to one folder. Omit for the account root. |  |
**workspace_id** | Option<**String**> |  |  |
**organization_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**offset** | Option<**i32**> |  |  |[default to 0]
**sort_by** | Option<**String**> |  |  |
**sort_order** | Option<**String**> |  |  |

### Return type

[**models::FilesAndFoldersResponse**](FilesAndFoldersResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## move_file

> models::MoveFileResponse move_file(id, move_file_request, account_id, x_workspace_id)
Move a single file to a target folder.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | File id. | [required] |
**move_file_request** | [**MoveFileRequest**](MoveFileRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::MoveFileResponse**](MoveFileResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_files

> models::SearchFilesResponse search_files(query, account_id, provider, folder_id, workspace_id, organization_id, limit, offset)
Substring-match search across the caller's files.

In-memory search — the platform lists up to ~500 files and filters locally on `name` (case-insensitive substring). Not suitable for global search across very large file libraries. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**folder_id** | Option<**String**> | Filter to one folder. Omit for the account root. |  |
**workspace_id** | Option<**String**> |  |  |
**organization_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**offset** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::SearchFilesResponse**](SearchFilesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_file

> models::SpatioFile update_file(id, update_file_request, account_id, x_workspace_id)
Update a file's metadata (name, folder, custom fields).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | File id. | [required] |
**update_file_request** | [**UpdateFileRequest**](UpdateFileRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_chunked_block

> models::UploadChunkedBlockResponse upload_chunked_block(session_id, block_hash, block, block_index)
Upload one block for an open chunked-upload session.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**session_id** | **String** |  | [required] |
**block_hash** | **String** |  | [required] |
**block** | **std::path::PathBuf** |  | [required] |
**block_index** | Option<**i32**> |  |  |

### Return type

[**models::UploadChunkedBlockResponse**](UploadChunkedBlockResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_file

> models::SpatioFile upload_file(file, folder_id, workspace_id, organization_id, account_id)
Upload a file via multipart form.

Multipart upload. Form field `file` carries the binary; auxiliary form fields scope the upload (`folderId`, `workspaceId`, `organizationId`, `accountId`). Max body size is currently 100 MB. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file** | **std::path::PathBuf** | File bytes (multipart form field name `file`). | [required] |
**folder_id** | Option<**String**> |  |  |
**workspace_id** | Option<**String**> |  |  |
**organization_id** | Option<**String**> |  |  |
**account_id** | Option<**String**> |  |  |

### Return type

[**models::SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_file_base64

> models::SpatioFile upload_file_base64(upload_file_base64_request)
Upload a file via JSON with base64-encoded content.

Equivalent to `uploadFile` for clients that can't post multipart bodies (e.g. browser fetch with strict CSP). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**upload_file_base64_request** | [**UploadFileBase64Request**](UploadFileBase64Request.md) |  | [required] |

### Return type

[**models::SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_commit_chunked_upload

> std::collections::HashMap<String, serde_json::Value> workspace_commit_chunked_upload(org, workspace, request_body)
Workspace-scoped chunked-upload commit (RBAC-protected).

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


## workspace_create_file_folder

> std::collections::HashMap<String, serde_json::Value> workspace_create_file_folder(org, workspace, request_body)
Workspace-scoped create-folder (RBAC-protected).

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


## workspace_delete_file

> workspace_delete_file(org, workspace, id)
Workspace-scoped delete-file.

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


## workspace_get_file

> std::collections::HashMap<String, serde_json::Value> workspace_get_file(org, workspace, id)
Workspace-scoped get-file.

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


## workspace_get_file_download

> std::collections::HashMap<String, serde_json::Value> workspace_get_file_download(org, workspace, id)
Workspace-scoped signed-download URL.

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


## workspace_get_file_manifest

> std::collections::HashMap<String, serde_json::Value> workspace_get_file_manifest(org, workspace, id)
Workspace-scoped chunked-file manifest.

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


## workspace_init_chunked_upload

> std::collections::HashMap<String, serde_json::Value> workspace_init_chunked_upload(org, workspace, request_body)
Workspace-scoped chunked-upload init (RBAC-protected).

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


## workspace_list_file_folders

> std::collections::HashMap<String, serde_json::Value> workspace_list_file_folders(org, workspace)
Workspace-scoped list-folders (RBAC-protected).

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


## workspace_list_files

> std::collections::HashMap<String, serde_json::Value> workspace_list_files(org, workspace)
Workspace-scoped list-files (RBAC-protected).

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


## workspace_move_file

> std::collections::HashMap<String, serde_json::Value> workspace_move_file(org, workspace, id, request_body)
Workspace-scoped move-file.

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


## workspace_update_file

> std::collections::HashMap<String, serde_json::Value> workspace_update_file(org, workspace, id, request_body)
Workspace-scoped update-file.

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


## workspace_upload_chunked_block

> std::collections::HashMap<String, serde_json::Value> workspace_upload_chunked_block(org, workspace, body)
Workspace-scoped chunked-upload block (RBAC-protected).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**body** | **std::path::PathBuf** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/octet-stream
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_upload_file

> std::collections::HashMap<String, serde_json::Value> workspace_upload_file(org, workspace, file)
Workspace-scoped multipart upload (RBAC-protected).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**workspace** | **String** |  | [required] |
**file** | Option<**std::path::PathBuf**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## workspace_upload_file_base64

> std::collections::HashMap<String, serde_json::Value> workspace_upload_file_base64(org, workspace, request_body)
Workspace-scoped base64 upload (RBAC-protected).

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

