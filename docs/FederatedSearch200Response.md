# FederatedSearch200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**Vec<models::FederatedSearch200ResponseItemsInner>**](FederatedSearch200ResponseItemsInner.md) |  | 
**next_page_tokens** | Option<**std::collections::HashMap<String, String>**> |  | [optional]
**per_platform** | [**std::collections::HashMap<String, models::FederatedSearch200ResponsePerPlatformValue>**](FederatedSearch200ResponsePerPlatformValue.md) |  | 
**errors** | Option<**std::collections::HashMap<String, String>**> | Per-platform errors. Other platforms still return results. | [optional]
**total_returned** | **i32** |  | 
**took** | **String** | Aggregate wall-clock time for the fan-out, e.g. \"120ms\". | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


