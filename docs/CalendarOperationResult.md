# CalendarOperationResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**data** | Option<**serde_json::Value**> | Operation-specific payload. See the operation's response description for the concrete shape.  | [optional]
**errors** | Option<[**Vec<models::CalendarAccountError>**](CalendarAccountError.md)> |  | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


