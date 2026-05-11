# \ContactsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**assign_contact_category**](ContactsApi.md#assign_contact_category) | **POST** /v1/contacts/{id}/categories | Assign a category to a contact.
[**create_contact**](ContactsApi.md#create_contact) | **POST** /v1/contacts | Create a contact.
[**create_contact_category**](ContactsApi.md#create_contact_category) | **POST** /v1/contacts/categories | Create a contact category.
[**delete_contact**](ContactsApi.md#delete_contact) | **DELETE** /v1/contacts/{id} | Delete a contact.
[**delete_contact_category**](ContactsApi.md#delete_contact_category) | **DELETE** /v1/contacts/categories/{id} | Delete a category.
[**get_contact**](ContactsApi.md#get_contact) | **GET** /v1/contacts/{id} | Fetch a contact.
[**list_contact_categories**](ContactsApi.md#list_contact_categories) | **GET** /v1/contacts/categories | List contact categories. Requires `organization_id` query param.
[**list_contact_providers**](ContactsApi.md#list_contact_providers) | **GET** /v1/contacts/providers | List supported contact providers (native + OAuth-connected).
[**list_contacts**](ContactsApi.md#list_contacts) | **GET** /v1/contacts | List the caller's contacts (across providers).
[**unassign_contact_category**](ContactsApi.md#unassign_contact_category) | **DELETE** /v1/contacts/{id}/categories/{categoryId} | Remove a category from a contact.
[**update_contact**](ContactsApi.md#update_contact) | **PATCH** /v1/contacts/{id} | Update a contact.
[**update_contact_category**](ContactsApi.md#update_contact_category) | **PATCH** /v1/contacts/categories/{id} | Update a category.



## assign_contact_category

> assign_contact_category(id, assign_contact_category_request)
Assign a category to a contact.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**assign_contact_category_request** | [**AssignContactCategoryRequest**](AssignContactCategoryRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_contact

> models::Contact create_contact(create_contact_request)
Create a contact.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_contact_request** | [**CreateContactRequest**](CreateContactRequest.md) |  | [required] |

### Return type

[**models::Contact**](Contact.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_contact_category

> models::ContactCategory create_contact_category(create_contact_category_request)
Create a contact category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_contact_category_request** | [**CreateContactCategoryRequest**](CreateContactCategoryRequest.md) |  | [required] |

### Return type

[**models::ContactCategory**](ContactCategory.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_contact

> delete_contact(id)
Delete a contact.

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


## delete_contact_category

> delete_contact_category(id)
Delete a category.

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


## get_contact

> models::Contact get_contact(id)
Fetch a contact.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::Contact**](Contact.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_contact_categories

> models::ContactCategoryListResponse list_contact_categories(organization_id)
List contact categories. Requires `organization_id` query param.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**organization_id** | **String** |  | [required] |

### Return type

[**models::ContactCategoryListResponse**](ContactCategoryListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_contact_providers

> models::ContactProviderListResponse list_contact_providers()
List supported contact providers (native + OAuth-connected).

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ContactProviderListResponse**](ContactProviderListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_contacts

> models::ContactListResponse list_contacts(limit, provider, search)
List the caller's contacts (across providers).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> |  |  |
**provider** | Option<**String**> |  |  |
**search** | Option<**String**> |  |  |

### Return type

[**models::ContactListResponse**](ContactListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unassign_contact_category

> unassign_contact_category(id, category_id)
Remove a category from a contact.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**category_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_contact

> models::Contact update_contact(id, update_contact_request)
Update a contact.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_contact_request** | [**UpdateContactRequest**](UpdateContactRequest.md) |  | [required] |

### Return type

[**models::Contact**](Contact.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_contact_category

> models::ContactCategory update_contact_category(id, update_contact_category_request)
Update a category.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_contact_category_request** | [**UpdateContactCategoryRequest**](UpdateContactCategoryRequest.md) |  | [required] |

### Return type

[**models::ContactCategory**](ContactCategory.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

