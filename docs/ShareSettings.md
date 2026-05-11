# ShareSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_public** | **bool** |  | 
**has_password** | **bool** |  | 
**share_token** | Option<**String**> | Opaque token embedded in the public URL. Empty when `isPublic` is false.  | [optional]
**share_url** | Option<**String**> | Fully-qualified public viewer URL. Computed server-side from `PUBLIC_VIEWER_BASE` (defaults to `https://spatio.app`) and the share token. Empty when the note is private.  | [optional]
**password_set_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> | When the current password was set, if any. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


