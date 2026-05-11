# Organization

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**name** | **String** |  | 
**slug** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**logo_url** | Option<**String**> |  | [optional]
**role** | **String** | The caller's role in this org (`owner`, `admin`, `billing_admin`, `member`). | 
**member_count** | Option<**i32**> |  | [optional]
**workspace_count** | Option<**i32**> |  | [optional]
**workspaces** | Option<[**Vec<models::OrganizationWorkspacesInner>**](OrganizationWorkspacesInner.md)> | Compact workspace summaries embedded in the org-list response. | [optional]
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


