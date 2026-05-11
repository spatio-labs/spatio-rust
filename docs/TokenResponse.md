# TokenResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_token** | **String** | Opaque bearer token. Format `tok_<32 random base64url>`. | 
**token_type** | **String** |  | 
**expires_in** | **i32** | Seconds until access_token expires. | 
**refresh_token** | Option<**String**> |  | [optional]
**scope** | Option<**String**> |  | [optional]
**id_token** | Option<**String**> | Only present when `openid` scope was granted. RS256-signed JWT — verify against the JWKS. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


