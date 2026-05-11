# RichTextObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: text, mention, equation) | 
**text** | Option<**String**> |  | [optional]
**annotations** | Option<[**models::TextAnnotations**](TextAnnotations.md)> |  | [optional]
**href** | Option<**String**> | External URL (`https://…`) or internal note anchor (`#blockId`, `#heading-slug`). Internal anchors resolve to the matching block in the same note.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


