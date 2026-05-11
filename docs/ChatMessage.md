# ChatMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**provider** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**channel_id** | **String** |  | 
**user_id** | **String** |  | 
**text** | **String** |  | 
**thread_id** | Option<**String**> | Set on replies and on parent messages once a thread exists.  | [optional]
**timestamp** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**reply_count** | Option<**i32**> |  | [optional]
**extra** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Provider-specific extras. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


