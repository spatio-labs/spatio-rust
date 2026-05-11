# FederatedSearchRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **String** |  | 
**platforms** | Option<**Vec<Platforms>**> | Subset to fan out to. Empty means all available platforms. (enum: notes, tasks, mail, calendar, files) | [optional]
**limit** | Option<**i32**> |  | [optional][default to 25]
**page_tokens** | Option<**std::collections::HashMap<String, String>**> | Per-platform cursor for pagination. | [optional]
**workspace_id** | Option<**String**> |  | [optional]
**organization_id** | Option<**String**> |  | [optional]
**include_shared** | Option<**bool**> |  | [optional]
**include_archived** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


