# PublicInvitationPayload

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **Kind** |  (enum: workspace, organization) | 
**id** | **String** |  | 
**workspace_id** | Option<**String**> |  | [optional]
**organization_id** | Option<**String**> |  | [optional]
**email** | **String** |  | 
**role** | **String** |  | 
**status** | **Status** |  (enum: pending, accepted, revoked, expired) | 
**expires_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**created_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**workspace** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**organization** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**invited_by** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


