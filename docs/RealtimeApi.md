# \RealtimeApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**issue_collaboration_token**](RealtimeApi.md#issue_collaboration_token) | **POST** /v1/realtime/collaboration-token | Exchange a bearer token for a short-lived Yjs collaboration JWT.



## issue_collaboration_token

> models::IssueCollaborationToken200Response issue_collaboration_token(issue_collaboration_token_request)
Exchange a bearer token for a short-lived Yjs collaboration JWT.

The Yjs Cloudflare Worker that powers live document collaboration (`wss://realtime-collaboration.<account>.workers.dev`) only accepts platform-signed JWTs. Third-party clients holding an OAuth access token or PAT call this endpoint to mint a 5-minute collaboration JWT they can present to the worker.  The minted JWT inherits user + workspace identity from the presenting bearer token. Optionally scope it to a single room by supplying `room` in the request body. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**issue_collaboration_token_request** | Option<[**IssueCollaborationTokenRequest**](IssueCollaborationTokenRequest.md)> |  |  |

### Return type

[**models::IssueCollaborationToken200Response**](issueCollaborationToken_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

