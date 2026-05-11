# Block

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**note_id** | **String** |  | 
**parent_id** | Option<**String**> |  | [optional]
**r#type** | [**models::BlockType**](BlockType.md) |  | 
**content** | [**models::BlockContent**](BlockContent.md) |  | 
**properties** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**position** | **i32** | Order within the parent (0-indexed). | 
**has_children** | **bool** |  | 
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


