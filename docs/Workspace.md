# Workspace

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**name** | **String** |  | 
**slug** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**logo_url** | Option<**String**> |  | [optional]
**organization_id** | Option<**String**> |  | [optional]
**organization** | Option<[**models::WorkspaceOrganization**](WorkspaceOrganization.md)> |  | [optional]
**role** | Option<**String**> | The caller's role in this workspace (`owner`, `admin`, `member`, `guest`). | [optional]
**settings** | Option<**serde_json::Value**> | Per-workspace settings. Currently emitted as either an object (`{language, timezone, ...}`) on `GET /v1/workspaces/{id}` or a JSON-encoded string on `GET /v1/organizations/{id}/workspaces`. Treat as opaque and parse defensively.  | [optional]
**is_default** | Option<**bool**> |  | [optional]
**member_count** | Option<**i32**> |  | [optional]
**billing_tier** | Option<**String**> |  | [optional]
**created_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**updated_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


