# Channel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**provider** | Option<**String**> | Registered provider id (e.g. `slack`, `native-chat`).  | [optional]
**account_id** | Option<**String**> |  | [optional]
**name** | **String** |  | 
**r#type** | **String** | Provider-specific. Common canonicals: `channel` and `private` (group channels), `im` (1:1 DM), `mpim` (group DM).  | 
**description** | Option<**String**> |  | [optional]
**topic** | Option<**String**> |  | [optional]
**is_member** | **bool** |  | 
**is_archived** | **bool** |  | 
**member_count** | Option<**i32**> |  | [optional]
**created_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


