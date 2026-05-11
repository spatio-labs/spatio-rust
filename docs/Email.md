# Email

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**thread_id** | Option<**String**> |  | [optional]
**provider** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**subject** | **String** |  | 
**from** | **String** |  | 
**to** | **Vec<String>** |  | 
**cc** | Option<**Vec<String>**> |  | [optional]
**bcc** | Option<**Vec<String>**> |  | [optional]
**body** | **String** |  | 
**html** | **bool** | `true` when `body` contains HTML, `false` for plain text.  | 
**date** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**labels** | Option<**Vec<String>**> |  | [optional]
**is_read** | **bool** |  | 
**is_starred** | **bool** |  | 
**attachments** | Option<[**Vec<models::AttachmentMeta>**](AttachmentMeta.md)> |  | [optional]
**snippet** | Option<**String**> |  | [optional]
**message_id** | Option<**String**> | RFC 5322 Message-ID header. | [optional]
**in_reply_to** | Option<**String**> | RFC 5322 In-Reply-To header — the parent message id this message is a reply to.  | [optional]
**references** | Option<**Vec<String>**> | RFC 5322 References header (ancestor chain). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


