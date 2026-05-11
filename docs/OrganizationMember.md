# OrganizationMember

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | `OrganizationMember` row id. | 
**user_id** | **String** |  | 
**role** | **Role** |  (enum: owner, admin, billing_admin, member) | 
**joined_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**invited_by** | Option<[**models::OrganizationMemberInvitedBy**](OrganizationMemberInvitedBy.md)> |  | [optional]
**user** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Embedded user-profile fields (id, email, name, profilePhoto, ...). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


