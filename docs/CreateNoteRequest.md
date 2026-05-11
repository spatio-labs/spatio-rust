# CreateNoteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **String** |  | 
**content** | Option<**String**> |  | [optional]
**icon** | Option<**String**> |  | [optional]
**cover_image** | Option<**String**> |  | [optional]
**parent_id** | Option<**String**> |  | [optional]
**properties** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**account_id** | Option<**String**> | Optional override for the target connected account. May also be passed as a `?accountId=` query param.  | [optional]
**provider** | Option<**String**> | Optional provider id (alternative to `accountId` when only one account exists for the provider). May also be passed as a `?provider=` query param.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


