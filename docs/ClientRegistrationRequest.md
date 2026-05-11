# ClientRegistrationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_name** | **String** |  | 
**redirect_uris** | **Vec<String>** |  | 
**grant_types** | Option<**Vec<String>**> |  | [optional][default to ["authorization_code","refresh_token"]]
**response_types** | Option<**Vec<String>**> |  | [optional][default to ["code"]]
**scope** | Option<**String**> | Space-separated scope list. Defaults to `read:*`. | [optional]
**token_endpoint_auth_method** | Option<**TokenEndpointAuthMethod**> |  (enum: none, client_secret_basic, client_secret_post) | [optional][default to None]
**client_uri** | Option<**String**> |  | [optional]
**logo_uri** | Option<**String**> |  | [optional]
**policy_uri** | Option<**String**> |  | [optional]
**tos_uri** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


