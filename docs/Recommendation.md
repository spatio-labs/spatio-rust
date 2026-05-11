# Recommendation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**workspace_id** | Option<**String**> |  | [optional]
**user_id** | Option<**String**> |  | [optional]
**kind** | Option<**String**> | Provider-tagged proposal kind (e.g. `note.draft`, `task.followup`). | [optional]
**title** | Option<**String**> |  | [optional]
**body** | Option<**String**> |  | [optional]
**status** | **Status** |  (enum: pending, accepted, dismissed, expired) | 
**payload** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**created_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**updated_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**expires_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


