# \RecommendationsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_recommendation**](RecommendationsApi.md#delete_recommendation) | **DELETE** /v1/recommendations/{id} | Delete a recommendation (hard delete; status-update is preferred).
[**get_recommendation**](RecommendationsApi.md#get_recommendation) | **GET** /v1/recommendations/{id} | Fetch one recommendation.
[**list_recommendations**](RecommendationsApi.md#list_recommendations) | **GET** /v1/recommendations | List recommendations for a workspace.
[**propose_recommendation**](RecommendationsApi.md#propose_recommendation) | **POST** /v1/recommendations | Agent-side propose endpoint (the `spatio_recommendations propose` MCP tool calls this).
[**update_recommendation_status**](RecommendationsApi.md#update_recommendation_status) | **PATCH** /v1/recommendations/{id}/status | Accept or dismiss a recommendation.



## delete_recommendation

> delete_recommendation(id)
Delete a recommendation (hard delete; status-update is preferred).

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


## get_recommendation

> models::Recommendation get_recommendation(id)
Fetch one recommendation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::Recommendation**](Recommendation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_recommendations

> models::RecommendationListResponse list_recommendations(workspace_id, status, limit)
List recommendations for a workspace.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | Option<**String**> |  |  |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |

### Return type

[**models::RecommendationListResponse**](RecommendationListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## propose_recommendation

> models::Recommendation propose_recommendation(propose_recommendation_request)
Agent-side propose endpoint (the `spatio_recommendations propose` MCP tool calls this).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**propose_recommendation_request** | [**ProposeRecommendationRequest**](ProposeRecommendationRequest.md) |  | [required] |

### Return type

[**models::Recommendation**](Recommendation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_recommendation_status

> models::Recommendation update_recommendation_status(id, update_recommendation_status_request)
Accept or dismiss a recommendation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_recommendation_status_request** | [**UpdateRecommendationStatusRequest**](UpdateRecommendationStatusRequest.md) |  | [required] |

### Return type

[**models::Recommendation**](Recommendation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

