# \OAuthApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_jwks**](OAuthApi.md#get_jwks) | **GET** /.well-known/jwks.json | JSON Web Key Set for id_token verification (RFC 7517).
[**get_o_auth_discovery**](OAuthApi.md#get_o_auth_discovery) | **GET** /.well-known/oauth-authorization-server | OAuth 2.1 authorization server metadata (RFC 8414).
[**get_open_id_configuration**](OAuthApi.md#get_open_id_configuration) | **GET** /.well-known/openid-configuration | OpenID Connect Discovery 1.0 metadata.
[**get_user_info**](OAuthApi.md#get_user_info) | **GET** /oauth2/userinfo | OIDC UserInfo (OpenID Connect Core 1.0 §5.3).
[**oauth_authorize**](OAuthApi.md#oauth_authorize) | **GET** /oauth2/authorize | OAuth 2.1 authorization endpoint (RFC 6749 + 7636 PKCE).
[**oauth_introspect**](OAuthApi.md#oauth_introspect) | **POST** /oauth2/introspect | RFC 7662 token introspection. Accepts both OAuth access tokens and PATs.
[**oauth_revoke**](OAuthApi.md#oauth_revoke) | **POST** /oauth2/revoke | RFC 7009 token revocation. Idempotent.
[**oauth_token**](OAuthApi.md#oauth_token) | **POST** /oauth2/token | Exchange authorization code or refresh token for an access token (+ id_token if `openid` scope).
[**post_user_info**](OAuthApi.md#post_user_info) | **POST** /oauth2/userinfo | Same as GET /oauth2/userinfo. Provided for clients that send the bearer in the body.
[**register_o_auth_client**](OAuthApi.md#register_o_auth_client) | **POST** /oauth2/register | Register a new OAuth 2.1 client (RFC 7591 dynamic client registration).



## get_jwks

> models::Jwks get_jwks()
JSON Web Key Set for id_token verification (RFC 7517).

The set of public keys RPs use to verify Spatio-issued id_tokens. Cached for 5 minutes at the edge. Always includes the currently-active signing key plus any retired keys that may still be in circulation (id_token TTL is 1 hour + slack). 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::Jwks**](JWKS.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_o_auth_discovery

> models::DiscoveryDocument get_o_auth_discovery()
OAuth 2.1 authorization server metadata (RFC 8414).

Returns the canonical metadata for the Spatio OAuth 2.1 + OpenID Connect server. Third-party RPs use this to auto-discover endpoint URLs, supported scopes, and signing algorithms.  Identical payload to `/.well-known/openid-configuration` — either path is acceptable; OIDC clients prefer the openid-configuration alias. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::DiscoveryDocument**](DiscoveryDocument.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_open_id_configuration

> models::DiscoveryDocument get_open_id_configuration()
OpenID Connect Discovery 1.0 metadata.

Alias of `/.well-known/oauth-authorization-server`. Provided so OIDC client libraries (NextAuth, Auth.js, oidc-client-ts, passport-openidconnect) auto-detect Spatio as an OIDC provider via their `wellKnown` / `discoveryUrl` config field. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::DiscoveryDocument**](DiscoveryDocument.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_user_info

> models::UserInfoResponse get_user_info()
OIDC UserInfo (OpenID Connect Core 1.0 §5.3).

Returns user claims gated by the scopes on the presenting access token. `sub` is always returned; `email`, `name`, etc. require their respective scopes. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::UserInfoResponse**](UserInfoResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## oauth_authorize

> oauth_authorize(client_id, redirect_uri, response_type, code_challenge, code_challenge_method, scope, state, nonce, prompt, max_age)
OAuth 2.1 authorization endpoint (RFC 6749 + 7636 PKCE).

Browser-redirect endpoint. Validates the client + redirect_uri, packs the request into a signed JWT, and 302s the user's browser to the consent UI. The consent UI then POSTs to `/oauth2/authorize/confirm` with the user's decision.  OIDC additions: `scope=openid+profile+email`, `nonce`, `prompt` (none|login|consent), `max_age`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**client_id** | **String** |  | [required] |
**redirect_uri** | **String** |  | [required] |
**response_type** | **String** |  | [required] |
**code_challenge** | **String** |  | [required] |
**code_challenge_method** | **String** |  | [required] |
**scope** | Option<**String**> |  |  |
**state** | Option<**String**> |  |  |
**nonce** | Option<**String**> |  |  |
**prompt** | Option<**String**> |  |  |
**max_age** | Option<**i32**> |  |  |

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## oauth_introspect

> models::IntrospectionResponse oauth_introspect(token)
RFC 7662 token introspection. Accepts both OAuth access tokens and PATs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** |  | [required] |

### Return type

[**models::IntrospectionResponse**](IntrospectionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## oauth_revoke

> oauth_revoke(token)
RFC 7009 token revocation. Idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## oauth_token

> models::TokenResponse oauth_token(grant_type, code, code_verifier, redirect_uri, refresh_token, client_id, client_secret)
Exchange authorization code or refresh token for an access token (+ id_token if `openid` scope).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**grant_type** | **String** |  | [required] |
**code** | Option<**String**> | Required for authorization_code grant. |  |
**code_verifier** | Option<**String**> | PKCE verifier — required for authorization_code grant. |  |
**redirect_uri** | Option<**String**> |  |  |
**refresh_token** | Option<**String**> | Required for refresh_token grant. |  |
**client_id** | Option<**String**> |  |  |
**client_secret** | Option<**String**> |  |  |

### Return type

[**models::TokenResponse**](TokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/x-www-form-urlencoded
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## post_user_info

> models::UserInfoResponse post_user_info()
Same as GET /oauth2/userinfo. Provided for clients that send the bearer in the body.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::UserInfoResponse**](UserInfoResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## register_o_auth_client

> models::ClientRegistrationResponse register_o_auth_client(client_registration_request)
Register a new OAuth 2.1 client (RFC 7591 dynamic client registration).

Returns a fresh `client_id` (and, for confidential clients, `client_secret`) plus a one-time `registration_access_token` the client can use later to update its registration. Public clients (mobile, SPA) MUST use `token_endpoint_auth_method: none` and PKCE.  Rate-limited to 10 registrations per hour per source IP. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**client_registration_request** | [**ClientRegistrationRequest**](ClientRegistrationRequest.md) |  | [required] |

### Return type

[**models::ClientRegistrationResponse**](ClientRegistrationResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

