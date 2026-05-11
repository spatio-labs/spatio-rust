# AccountStatus

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **String** | Provider id (e.g. `native-notes`, `notion`, `google-keep`). | 
**account_id** | **String** | Connected-account row id. | 
**account_name** | Option<**String**> | Human-readable label for the account, when available. | [optional]
**status** | **Status** | - `ok` — provider call returned without error. - `error` — provider call failed; details in `error`. - `skipped` — connection was filtered out before the provider   call ran. Reserved; not currently emitted by the runtime.  (enum: ok, error, skipped) | 
**error** | Option<[**models::AccountError**](AccountError.md)> |  | [optional]
**next_page_token** | Option<**String**> | Provider-specific cursor for the next page, if any. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


