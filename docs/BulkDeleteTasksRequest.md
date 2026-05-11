# BulkDeleteTasksRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_ids** | Option<**Vec<String>**> |  | [optional]
**account_ids** | Option<**Vec<String>**> | Parallel slice with taskIds — accountIds[i] targets taskIds[i]. | [optional]
**task_id** | Option<**String**> | Singular fallback when only deleting one task. | [optional]
**account_id** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


