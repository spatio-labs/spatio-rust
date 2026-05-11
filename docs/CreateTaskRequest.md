# CreateTaskRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**due_date** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**priority** | Option<**Priority**> |  (enum: none, low, medium, high, urgent) | [optional]
**labels** | Option<**Vec<String>**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**assignee_id** | Option<**String**> |  | [optional]
**parent_task_id** | Option<**String**> |  | [optional]
**r#type** | Option<**String**> |  | [optional]
**source_platform** | Option<**String**> |  | [optional]
**source_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | Optional override for the target connected account. May also be passed as `?accountId=`.  | [optional]
**provider** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


