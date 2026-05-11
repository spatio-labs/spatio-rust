# CreateDraftRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**to** | Option<**Vec<String>**> |  | [optional]
**cc** | Option<**Vec<String>**> |  | [optional]
**bcc** | Option<**Vec<String>**> |  | [optional]
**subject** | Option<**String**> |  | [optional]
**body** | Option<**String**> |  | [optional]
**html** | Option<**bool**> |  | [optional]
**attachments** | Option<[**Vec<models::AttachmentInput>**](AttachmentInput.md)> |  | [optional]
**thread_id** | Option<**String**> | Provider thread id — set when this draft is a reply, so the sent message lands inside the parent thread.  | [optional]
**in_reply_to** | Option<**String**> |  | [optional]
**references** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


