# \SheetsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_sheet**](SheetsApi.md#create_sheet) | **POST** /v1/sheets | Create a sheet.
[**create_sheet_row**](SheetsApi.md#create_sheet_row) | **POST** /v1/sheets/{id}/rows | Insert a row.
[**delete_sheet**](SheetsApi.md#delete_sheet) | **DELETE** /v1/sheets/{id} | Delete a sheet.
[**delete_sheet_row**](SheetsApi.md#delete_sheet_row) | **DELETE** /v1/sheets/{id}/rows/{rowIndex} | Delete a row.
[**get_sheet**](SheetsApi.md#get_sheet) | **GET** /v1/sheets/{id} | Fetch one sheet.
[**list_sheet_rows**](SheetsApi.md#list_sheet_rows) | **GET** /v1/sheets/{id}/rows | List rows in a sheet.
[**list_sheets**](SheetsApi.md#list_sheets) | **GET** /v1/sheets | List sheets across connected accounts.
[**update_sheet**](SheetsApi.md#update_sheet) | **PATCH** /v1/sheets/{id} | Update a sheet (partial).
[**update_sheet_cell**](SheetsApi.md#update_sheet_cell) | **PATCH** /v1/sheets/{id}/rows/{rowIndex}/cells/{column} | Update a single cell.
[**update_sheet_row**](SheetsApi.md#update_sheet_row) | **PATCH** /v1/sheets/{id}/rows/{rowIndex} | Update a row (sparse).



## create_sheet

> models::Sheet create_sheet(create_sheet_request, account_id, provider, x_workspace_id)
Create a sheet.

Creates a new sheet under the target account. Target resolution mirrors `POST /v1/notes`: body `accountId` → `?accountId=` → body `provider` → `?provider=` → caller's single connected account (errors with `ambiguous_account` if more than one is connected and no selector is supplied). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_sheet_request** | [**CreateSheetRequest**](CreateSheetRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Sheet**](Sheet.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_sheet_row

> models::Row create_sheet_row(id, create_row_request, account_id, x_workspace_id)
Insert a row.

Inserts a row at `index` (zero-based) or appends to the end when `index` is omitted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
**create_row_request** | [**CreateRowRequest**](CreateRowRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Row**](Row.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_sheet

> models::SuccessFlag delete_sheet(id, account_id, x_workspace_id)
Delete a sheet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
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


## delete_sheet_row

> models::SuccessFlag delete_sheet_row(id, row_index, account_id, x_workspace_id)
Delete a row.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
**row_index** | **i32** | Zero-based row index. | [required] |
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


## get_sheet

> models::Sheet get_sheet(id, account_id, x_workspace_id)
Fetch one sheet.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Sheet**](Sheet.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sheet_rows

> models::RowList list_sheet_rows(id, account_id, x_workspace_id, limit, offset)
List rows in a sheet.

Single-account row list. Unlike `GET /v1/sheets`, row listing always targets the one account that owns the sheet, so the response is a plain `{ rows, total }` rather than a fan-out envelope. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |[default to 100]
**offset** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::RowList**](RowList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sheets

> models::SheetListEnvelope list_sheets(account_id, provider, x_workspace_id, limit, offset)
List sheets across connected accounts.

Fan-out list. Returns every sheet visible to the caller across every connected sheets provider, paginated by `limit` / `offset`. Pass `?accountId=` or `?provider=` to scope to a single source. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**provider** | Option<**String**> | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**offset** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::SheetListEnvelope**](SheetListEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_sheet

> models::Sheet update_sheet(id, update_sheet_request, account_id, x_workspace_id)
Update a sheet (partial).

Partial update of sheet metadata. The renderer also calls this via `PUT /v1/sheets/{id}` for autosave parity; both verbs invoke the same handler. Per-cell and per-row mutations live on their dedicated endpoints, not here. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
**update_sheet_request** | [**UpdateSheetRequest**](UpdateSheetRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Sheet**](Sheet.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_sheet_cell

> models::Cell update_sheet_cell(id, row_index, column, update_cell_request, account_id, x_workspace_id)
Update a single cell.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
**row_index** | **i32** | Zero-based row index. | [required] |
**column** | **String** | Column identifier. Provider-specific — usually a letter (`A`, `AB`) for spreadsheet providers or a column key string for structured providers.  | [required] |
**update_cell_request** | [**UpdateCellRequest**](UpdateCellRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Cell**](Cell.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_sheet_row

> models::Row update_sheet_row(id, row_index, update_row_request, account_id, x_workspace_id)
Update a row (sparse).

Sparse update — keys present in `cells` overwrite that column; keys absent are preserved. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Sheet id. | [required] |
**row_index** | **i32** | Zero-based row index. | [required] |
**update_row_request** | [**UpdateRowRequest**](UpdateRowRequest.md) |  | [required] |
**account_id** | Option<**String**> | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  |  |
**x_workspace_id** | Option<**String**> | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  |  |

### Return type

[**models::Row**](Row.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

