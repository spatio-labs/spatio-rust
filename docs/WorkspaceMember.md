# WorkspaceMember

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**role** | **Role** |  (enum: owner, admin, member, guest) | 
**email** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**avatar** | Option<**String**> |  | [optional]
**joined_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**user** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


