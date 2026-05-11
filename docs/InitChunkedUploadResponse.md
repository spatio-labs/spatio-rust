# InitChunkedUploadResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session_id** | **String** |  | 
**blocks_to_upload** | **Vec<String>** |  | 
**blocks_already_exist** | **Vec<String>** | Blocks the platform already has and the client can skip (content-addressed deduplication).  | 
**deduplication_pct** | **f64** |  | 
**estimated_upload_size** | **i64** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


