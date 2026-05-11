# Sheet

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**provider** | Option<**String**> | Registered provider id (e.g. `native-sheets`). | [optional]
**account_id** | Option<**String**> | Connected-account row this sheet belongs to. | [optional]
**owner_user_id** | Option<**String**> | User id of the sheet owner; non-native providers leave empty. | [optional]
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**data** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Free-form provider blob. Treat as opaque. | [optional]
**row_count** | **i32** |  | 
**column_count** | **i32** |  | 
**sheet_count** | **i32** | Tab count when the file contains multiple sheets. | 
**is_public** | **bool** |  | 
**is_read_only** | **bool** |  | 
**file_size** | Option<**i32**> |  | [optional]
**last_accessed_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


