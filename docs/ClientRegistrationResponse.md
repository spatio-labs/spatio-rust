# ClientRegistrationResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **String** |  | 
**client_secret** | Option<**String**> | Only returned when token_endpoint_auth_method is client_secret_*. | [optional]
**client_name** | **String** |  | 
**redirect_uris** | **Vec<String>** |  | 
**grant_types** | Option<**Vec<String>**> |  | [optional]
**response_types** | Option<**Vec<String>**> |  | [optional]
**scope** | Option<**String**> |  | [optional]
**token_endpoint_auth_method** | Option<**String**> |  | [optional]
**registration_access_token** | **String** |  | 
**registration_client_uri** | Option<**String**> |  | [optional]
**client_id_issued_at** | **i32** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


