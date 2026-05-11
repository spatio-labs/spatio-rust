# \SearchApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**federated_search**](SearchApi.md#federated_search) | **POST** /v1/search | Cross-platform federated search.



## federated_search

> models::FederatedSearch200Response federated_search(federated_search_request)
Cross-platform federated search.

Fans out to every platform's per-platform search method in parallel, merges + dedupes results, and returns them in a relevance-then-recency ranking with per-platform cursors for pagination. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**federated_search_request** | [**FederatedSearchRequest**](FederatedSearchRequest.md) |  | [required] |

### Return type

[**models::FederatedSearch200Response**](federatedSearch_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

