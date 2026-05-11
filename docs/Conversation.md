# Conversation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**user_id** | **String** |  | 
**title** | **String** |  | 
**context** | Option<**String**> | Free-form context tag (e.g. `sidebar:sheets:entity:<id>`). | [optional]
**cwd** | Option<**String**> |  | [optional]
**session_id** | Option<**String**> |  | [optional]
**pinned** | Option<**bool**> |  | [optional]
**last_message_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**message_count** | Option<**i32**> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**created_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**updated_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


