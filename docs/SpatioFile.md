# SpatioFile

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**provider** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**name** | **String** |  | 
**size** | **i64** | Bytes. | 
**mime_type** | **String** |  | 
**folder_id** | Option<**String**> |  | [optional]
**storage_type** | **String** | Backing storage class — `r2`, `gdrive`, `dropbox`, etc. Provider-specific; treat as opaque.  | 
**download_url** | Option<**String**> | Pre-signed download URL when one is cached on the row. Use `GET /v1/files/{id}/download` for a guaranteed-fresh URL — this field can lag past expiry.  | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


