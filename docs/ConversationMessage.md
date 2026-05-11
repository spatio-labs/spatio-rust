# ConversationMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**conversation_id** | **String** |  | 
**role** | **String** | `user`, `assistant`, `system`, or `tool`. | 
**content** | Option<**String**> |  | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**created_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


