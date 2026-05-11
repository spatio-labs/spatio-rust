# Note

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable provider id for the note. | 
**provider** | Option<**String**> | Registered provider id (e.g. `native-notes`). | [optional]
**account_id** | Option<**String**> | Connected-account row this note belongs to. | [optional]
**owner_user_id** | Option<**String**> | User id of the note's owner. Surfaced so the renderer can show \"Shared with you\" when `ownerUserId` differs from the viewer's id. Empty for non-native providers.  | [optional]
**title** | **String** |  | 
**content** | **String** | Markdown body. The block tree at `/v1/notes/{id}/blocks` is the canonical structured representation; `content` is a flattened markdown view kept for clients that don't render blocks.  | 
**icon** | Option<**String**> | Emoji or short string used as the note's icon. | [optional]
**cover_image** | Option<**String**> | URL of the note's cover image. | [optional]
**parent_id** | Option<**String**> | Parent note id when notes are nested. | [optional]
**properties** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Free-form provider-specific properties (tags, etc.). | [optional]
**archived** | **bool** |  | 
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**last_edited_by** | Option<**String**> | User id of the most recent editor. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


