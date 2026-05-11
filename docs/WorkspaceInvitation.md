# WorkspaceInvitation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**workspace_id** | Option<**String**> |  | [optional]
**email** | **String** |  | 
**role** | **String** |  | 
**expires_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**accepted_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**revoked_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**status** | Option<**Status**> |  (enum: pending, accepted, revoked, expired) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


