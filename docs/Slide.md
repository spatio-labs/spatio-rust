# Slide

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**provider** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**presentation_id** | **String** |  | 
**title** | **String** |  | 
**notes** | Option<**String**> | Speaker notes. | [optional]
**layout** | Option<**String**> | Free-form layout id. Provider-specific (`title`, `two-column`, `image-left`, custom). Not enumerated to avoid forcing a breaking change every time a provider adds one.  | [optional]
**background_color** | Option<**String**> |  | [optional]
**background_image_url** | Option<**String**> |  | [optional]
**text_color** | Option<**String**> |  | [optional]
**transition** | Option<**String**> | Free-form transition id. | [optional]
**position** | **i32** | Zero-based position within the presentation. | 
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


