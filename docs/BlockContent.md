# BlockContent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rich_text** | Option<[**Vec<models::RichTextObject>**](RichTextObject.md)> |  | [optional]
**language** | Option<**String**> | Programming language for `code` blocks. | [optional]
**checked** | Option<**bool**> | Toggle state for `to_do` blocks. | [optional]
**icon** | Option<**String**> | Emoji or short string for `callout` blocks. | [optional]
**color** | Option<**String**> | Theme color for `callout` blocks. | [optional]
**url** | Option<**String**> | Source URL for `image`, `video`, `file` blocks. | [optional]
**caption** | Option<**String**> | Visible caption for media blocks. | [optional]
**alt_text** | Option<**String**> | Screen-reader description for media blocks. Distinct from `caption` (visible to readers) — required for accessible notes when the image conveys meaning.  | [optional]
**embed_url** | Option<**String**> | Source URL for `embed` blocks. | [optional]
**cells** | Option<[**Vec<Vec<models::RichTextObject>>**](Vec.md)> | 2D rich-text grid for `table` and `table_row` blocks. | [optional]
**expression** | Option<**String**> | TeX/MathJax expression for `equation` blocks. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


