# OrganizationInvitation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**organization_id** | Option<**String**> |  | [optional]
**email** | **String** |  | 
**role** | **String** |  | 
**token** | Option<**String**> | Opaque invitation token (omitted on list responses). | [optional]
**expires_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**accepted_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**revoked_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**invited_by** | Option<[**models::OrganizationMemberInvitedBy**](OrganizationMemberInvitedBy.md)> |  | [optional]
**status** | Option<**Status**> |  (enum: pending, accepted, revoked, expired) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


