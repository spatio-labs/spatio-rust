# Task

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**provider** | Option<**String**> | Registered provider id (e.g. `native-tasks`, `linear`). | [optional]
**account_id** | Option<**String**> |  | [optional]
**owner_user_id** | Option<**String**> |  | [optional]
**title** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**status** | Option<**String**> | Free-form status string. Canonical values across most providers: `todo`, `in_progress`, `in_review`, `backlog`, `done`. The platform falls back to `done` when `completed` is true and `status` is empty, else `todo`.  | [optional]
**completed** | **bool** |  | 
**due_date** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**priority** | **Priority** | Priority bucket. Canonical values (mapped from a 0–4 integer): `none`, `low`, `medium`, `high`, `urgent`.  (enum: none, low, medium, high, urgent) | 
**labels** | Option<**Vec<String>**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**assignee_id** | Option<**String**> |  | [optional]
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**completed_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**parent_task_id** | Option<**String**> | Parent task id when this is a subtask. | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Provider-specific extras. | [optional]
**r#type** | Option<**String**> | Discriminator. Canonical values: `todo`, `reminder`, `issue`. Empty defaults to `todo`.  | [optional]
**source_platform** | Option<**String**> | When this task was auto-generated from another artifact (e.g. a calendar event reminder), the platform id of that artifact.  | [optional]
**source_id** | Option<**String**> | Source artifact id paired with `sourcePlatform`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


