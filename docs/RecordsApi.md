# \RecordsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_record**](RecordsApi.md#create_record) | **POST** /v1/records | Create a record.
[**create_record_type**](RecordsApi.md#create_record_type) | **POST** /v1/records/types | Create a record type (org-scoped).
[**delete_record**](RecordsApi.md#delete_record) | **DELETE** /v1/records/{id} | Delete a record.
[**get_record**](RecordsApi.md#get_record) | **GET** /v1/records/{id} | Fetch a record.
[**list_record_types**](RecordsApi.md#list_record_types) | **GET** /v1/records/types | List record types for an organization.
[**list_records**](RecordsApi.md#list_records) | **GET** /v1/records | List records for an organization. `organization_id` query param is required (handler returns 400 otherwise). 
[**update_record**](RecordsApi.md#update_record) | **PATCH** /v1/records/{id} | Update a record.
[**update_record_type**](RecordsApi.md#update_record_type) | **PATCH** /v1/records/types/{id} | Update a record type.



## create_record

> models::Record create_record(create_record_request)
Create a record.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_record_request** | [**CreateRecordRequest**](CreateRecordRequest.md) |  | [required] |

### Return type

[**models::Record**](Record.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_record_type

> models::RecordType create_record_type(create_record_type_request)
Create a record type (org-scoped).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_record_type_request** | [**CreateRecordTypeRequest**](CreateRecordTypeRequest.md) |  | [required] |

### Return type

[**models::RecordType**](RecordType.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_record

> delete_record(id)
Delete a record.

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


## get_record

> models::Record get_record(id)
Fetch a record.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::Record**](Record.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_record_types

> models::RecordTypeListResponse list_record_types(organization_id)
List record types for an organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**organization_id** | **String** |  | [required] |

### Return type

[**models::RecordTypeListResponse**](RecordTypeListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_records

> models::RecordListResponse list_records(organization_id, record_type_id, limit)
List records for an organization. `organization_id` query param is required (handler returns 400 otherwise). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**organization_id** | **String** |  | [required] |
**record_type_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |

### Return type

[**models::RecordListResponse**](RecordListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_record

> models::Record update_record(id, update_record_request)
Update a record.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_record_request** | [**UpdateRecordRequest**](UpdateRecordRequest.md) |  | [required] |

### Return type

[**models::Record**](Record.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_record_type

> models::RecordType update_record_type(id, update_record_type_request)
Update a record type.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_record_type_request** | [**UpdateRecordTypeRequest**](UpdateRecordTypeRequest.md) |  | [required] |

### Return type

[**models::RecordType**](RecordType.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

