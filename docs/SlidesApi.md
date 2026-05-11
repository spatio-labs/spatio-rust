# \SlidesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_presentation**](SlidesApi.md#create_presentation) | **POST** /v1/slides | Create a presentation.
[**create_slide**](SlidesApi.md#create_slide) | **POST** /v1/slides/{id}/slides | Insert a slide.
[**create_slide_element**](SlidesApi.md#create_slide_element) | **POST** /v1/slides/{id}/slides/{slideId}/elements | Add a canvas element (text/shape/image) to a slide.
[**delete_presentation**](SlidesApi.md#delete_presentation) | **DELETE** /v1/slides/{id} | Delete a presentation.
[**delete_slide**](SlidesApi.md#delete_slide) | **DELETE** /v1/slides/{id}/slides/{slideId} | Delete a slide.
[**delete_slide_element**](SlidesApi.md#delete_slide_element) | **DELETE** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Delete a slide element.
[**disable_presentation_share**](SlidesApi.md#disable_presentation_share) | **DELETE** /v1/slides/{id}/share | Disable public sharing.
[**enable_presentation_share**](SlidesApi.md#enable_presentation_share) | **POST** /v1/slides/{id}/share | Enable (or update password on) public sharing.
[**export_presentation_pdf**](SlidesApi.md#export_presentation_pdf) | **POST** /v1/slides/{id}/export/pdf | Render the presentation as a PDF.
[**export_presentation_pptx**](SlidesApi.md#export_presentation_pptx) | **POST** /v1/slides/{id}/export/pptx | Render the presentation as a PowerPoint (.pptx) file.
[**get_presentation**](SlidesApi.md#get_presentation) | **GET** /v1/slides/{id} | Fetch one presentation.
[**get_presentation_share_settings**](SlidesApi.md#get_presentation_share_settings) | **GET** /v1/slides/{id}/share | Fetch share settings for a presentation.
[**get_public_presentation**](SlidesApi.md#get_public_presentation) | **GET** /public/slides/{token} | Fetch a publicly shared presentation.
[**get_slide**](SlidesApi.md#get_slide) | **GET** /v1/slides/{id}/slides/{slideId} | Fetch one slide.
[**get_slide_element**](SlidesApi.md#get_slide_element) | **GET** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Fetch one slide element.
[**list_presentations**](SlidesApi.md#list_presentations) | **GET** /v1/slides | List presentations across connected accounts.
[**list_slide_elements**](SlidesApi.md#list_slide_elements) | **GET** /v1/slides/{id}/slides/{slideId}/elements | List the canvas elements on a slide.
[**list_slides_in_presentation**](SlidesApi.md#list_slides_in_presentation) | **GET** /v1/slides/{id}/slides | List slides in a presentation.
[**rotate_presentation_share_token**](SlidesApi.md#rotate_presentation_share_token) | **POST** /v1/slides/{id}/share/rotate | Rotate the share token, invalidating outstanding URLs.
[**update_presentation**](SlidesApi.md#update_presentation) | **PATCH** /v1/slides/{id} | Update presentation metadata (partial).
[**update_slide**](SlidesApi.md#update_slide) | **PATCH** /v1/slides/{id}/slides/{slideId} | Update a slide (partial).
[**update_slide_element**](SlidesApi.md#update_slide_element) | **PATCH** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Update a slide element (partial).



## create_presentation

> models::Presentation create_presentation(create_presentation_request, account_id, provider, x_workspace_id)
Create a presentation.

Creates a new deck under the target account. Target resolution mirrors `POST /v1/notes` and `/v1/sheets`: body `accountId` → `?accountId=` → body `provider` → `?provider=` → caller's single connected account (errors with `ambiguous_account` otherwise). The new deck is auto-seeded with one blank slide so the renderer has something to display immediately. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_presentation_request** | [**CreatePresentationRequest**](CreatePresentationRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Presentation**](Presentation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_slide

> models::Slide create_slide(id, create_slide_request, account_id, x_workspace_id)
Insert a slide.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**create_slide_request** | [**CreateSlideRequest**](CreateSlideRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Slide**](Slide.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_slide_element

> models::SlideElement create_slide_element(id, slide_id, create_slide_element_request, account_id, x_workspace_id)
Add a canvas element (text/shape/image) to a slide.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**create_slide_element_request** | [**CreateSlideElementRequest**](CreateSlideElementRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SlideElement**](SlideElement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_presentation

> models::SuccessFlag delete_presentation(id, account_id, x_workspace_id)
Delete a presentation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_slide

> models::SuccessFlag delete_slide(id, slide_id, account_id, x_workspace_id)
Delete a slide.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_slide_element

> models::SuccessFlag delete_slide_element(id, slide_id, element_id, account_id, x_workspace_id)
Delete a slide element.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**element_id** | **String** | Slide-element id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## disable_presentation_share

> disable_presentation_share(id, account_id, x_workspace_id)
Disable public sharing.

Owner-only. Subsequent public viewer requests 404.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_presentation_share

> models::ShareSettings enable_presentation_share(id, account_id, x_workspace_id, enable_share_request)
Enable (or update password on) public sharing.

Owner-only. With `setPassword: false` (or empty body), flips the deck public without changing the password. With `setPassword: true`, applies `password` (empty clears). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**enable_share_request** | Option<[**EnableShareRequest**](EnableShareRequest.md)> |  |  |

### Return type

[**models::ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## export_presentation_pdf

> std::path::PathBuf export_presentation_pdf(id, account_id, x_workspace_id, storage, filename, export_pdf_request)
Render the presentation as a PDF.

Proxies to the Spatio export sidecar (Playwright). Two response modes selected via `?storage=`:    - `stream` (default) — response body is the PDF binary     (`application/pdf`).   - `r2` — uploads the rendered PDF to R2 storage and returns     a JSON envelope with a 24-hour signed URL.  Returns `503 Service Unavailable` when the export sidecar is not configured (dev fallback to the client-side exporter). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**storage** | Option<**String**> |  |  |[default to stream]
**filename** | Option<**String**> | Sanitized base name for the downloaded PDF. |  |
**export_pdf_request** | Option<[**ExportPdfRequest**](ExportPdfRequest.md)> |  |  |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## export_presentation_pptx

> std::path::PathBuf export_presentation_pptx(id, account_id, x_workspace_id, storage, filename, export_pdf_request)
Render the presentation as a PowerPoint (.pptx) file.

Proxies to the Spatio export sidecar (Playwright + pptxgenjs). Each slide is screenshotted at 2× device-pixel ratio and wrapped into a PowerPoint .pptx as a full-bleed image. Visual fidelity is preserved exactly — what renders in Spatio renders identically in PowerPoint, Keynote, Google Slides — at the cost of in-PowerPoint editability of slide content. Users edit slide content back in Spatio (the source of truth), not inside PowerPoint.  Two response modes selected via `?storage=`:    - `stream` (default) — response body is the PPTX binary     (`application/vnd.openxmlformats-officedocument.presentationml.presentation`).   - `r2` — uploads the rendered PPTX to R2 storage and returns     a JSON envelope with a 24-hour signed URL.  Returns `503 Service Unavailable` when the export sidecar is not configured. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**storage** | Option<**String**> |  |  |[default to stream]
**filename** | Option<**String**> | Sanitized base name for the downloaded PPTX. |  |
**export_pdf_request** | Option<[**ExportPdfRequest**](ExportPdfRequest.md)> |  |  |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/vnd.openxmlformats-officedocument.presentationml.presentation, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_presentation

> models::Presentation get_presentation(id, account_id, x_workspace_id)
Fetch one presentation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Presentation**](Presentation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_presentation_share_settings

> models::ShareSettings get_presentation_share_settings(id, account_id, x_workspace_id)
Fetch share settings for a presentation.

Owner-only. Mirror of `GET /v1/notes/{id}/share` — same shape, same fields. Returns the current public-share configuration, including the share token and computed public viewer URL when the deck is currently public. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_public_presentation

> std::collections::HashMap<String, serde_json::Value> get_public_presentation(token, password)
Fetch a publicly shared presentation.

Unauthenticated. Mirror of `GET /public/notes/{token}`. The share token is the credential. For password-protected decks the password is supplied via `?password=`; the response distinguishes \"no password supplied\" from \"wrong password\" so the viewer can render the right prompt. Unknown tokens and disabled-share decks both return `404` to prevent enumeration. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**token** | **String** | Opaque public-share token. | [required] |
**password** | Option<**String**> | Optional viewer password. |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_slide

> models::Slide get_slide(id, slide_id, account_id, x_workspace_id)
Fetch one slide.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Slide**](Slide.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_slide_element

> models::SlideElement get_slide_element(id, slide_id, element_id, account_id, x_workspace_id)
Fetch one slide element.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**element_id** | **String** | Slide-element id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SlideElement**](SlideElement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_presentations

> models::PresentationListEnvelope list_presentations(account_id, provider, x_workspace_id, limit, offset)
List presentations across connected accounts.

Fan-out list. Returns every presentation visible to the caller across every connected slides provider. Pass `?accountId=` or `?provider=` to scope to a single source. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**offset** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::PresentationListEnvelope**](PresentationListEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_slide_elements

> models::SlideElementList list_slide_elements(id, slide_id, account_id, x_workspace_id)
List the canvas elements on a slide.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SlideElementList**](SlideElementList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_slides_in_presentation

> models::SlideList list_slides_in_presentation(id, account_id, x_workspace_id)
List slides in a presentation.

Single-account list. Returns slides in the order set by their `position` field. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SlideList**](SlideList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rotate_presentation_share_token

> models::ShareSettings rotate_presentation_share_token(id, account_id, x_workspace_id)
Rotate the share token, invalidating outstanding URLs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_presentation

> models::Presentation update_presentation(id, update_presentation_request, account_id, x_workspace_id)
Update presentation metadata (partial).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**update_presentation_request** | [**UpdatePresentationRequest**](UpdatePresentationRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Presentation**](Presentation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_slide

> models::Slide update_slide(id, slide_id, update_slide_request, account_id, x_workspace_id)
Update a slide (partial).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**update_slide_request** | [**UpdateSlideRequest**](UpdateSlideRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Slide**](Slide.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_slide_element

> models::SlideElement update_slide_element(id, slide_id, element_id, update_slide_element_request, account_id, x_workspace_id)
Update a slide element (partial).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Presentation id. | [required] |
**slide_id** | **String** | Slide id within the presentation. | [required] |
**element_id** | **String** | Slide-element id. | [required] |
**update_slide_element_request** | [**UpdateSlideElementRequest**](UpdateSlideElementRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::SlideElement**](SlideElement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

