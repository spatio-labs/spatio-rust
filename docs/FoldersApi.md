# \FoldersApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_email_folder**](FoldersApi.md#create_email_folder) | **POST** /v1/folders | Create an email folder.
[**delete_email_folder**](FoldersApi.md#delete_email_folder) | **DELETE** /v1/folders/{id} | Delete an email folder.
[**list_email_folders**](FoldersApi.md#list_email_folders) | **GET** /v1/folders | List the caller's email folders.
[**list_folder_emails**](FoldersApi.md#list_folder_emails) | **GET** /v1/folders/{id}/emails | List emails inside a folder.
[**move_emails_to_folder**](FoldersApi.md#move_emails_to_folder) | **POST** /v1/folders/{id}/emails | Move emails into a folder.
[**update_email_folder**](FoldersApi.md#update_email_folder) | **PUT** /v1/folders/{id} | Update an email folder.



## create_email_folder

> models::EmailFolder create_email_folder(create_email_folder_request)
Create an email folder.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_email_folder_request** | [**CreateEmailFolderRequest**](CreateEmailFolderRequest.md) |  | [required] |

### Return type

[**models::EmailFolder**](EmailFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_email_folder

> delete_email_folder(id)
Delete an email folder.

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


## list_email_folders

> models::EmailFolderListResponse list_email_folders()
List the caller's email folders.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::EmailFolderListResponse**](EmailFolderListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_folder_emails

> std::collections::HashMap<String, serde_json::Value> list_folder_emails(id)
List emails inside a folder.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## move_emails_to_folder

> std::collections::HashMap<String, serde_json::Value> move_emails_to_folder(id, move_emails_request)
Move emails into a folder.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**move_emails_request** | [**MoveEmailsRequest**](MoveEmailsRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_email_folder

> models::EmailFolder update_email_folder(id, update_email_folder_request)
Update an email folder.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_email_folder_request** | [**UpdateEmailFolderRequest**](UpdateEmailFolderRequest.md) |  | [required] |

### Return type

[**models::EmailFolder**](EmailFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

