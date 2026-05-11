# IssueCollaborationToken200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **String** | HS256 JWT, signed with the shared platform/worker secret. | 
**ws_url** | **String** | Base WebSocket URL of the Yjs worker. | 
**room** | Option<**String**> |  | [optional]
**expires_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**expires_in** | **i32** | Seconds until the token expires. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


