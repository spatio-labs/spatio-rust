# \OrganizationsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_organization_invitation**](OrganizationsApi.md#accept_organization_invitation) | **POST** /v1/organizations/{org}/accept-invitation | Accept an invitation to this organization.
[**add_organization_member**](OrganizationsApi.md#add_organization_member) | **POST** /v1/organizations/{org}/members | Add a member directly (skips invitation flow).
[**create_organization**](OrganizationsApi.md#create_organization) | **POST** /v1/organizations | Create an organization.
[**create_organization_concept**](OrganizationsApi.md#create_organization_concept) | **POST** /v1/organizations/{org}/concepts | Create an org-brain concept (admin+ only).
[**create_organization_custom_role**](OrganizationsApi.md#create_organization_custom_role) | **POST** /v1/organizations/{org}/roles | Create a custom role (admin+ only).
[**create_organization_invitation**](OrganizationsApi.md#create_organization_invitation) | **POST** /v1/organizations/{org}/invitations | Invite a user to the organization.
[**create_organization_workspace**](OrganizationsApi.md#create_organization_workspace) | **POST** /v1/organizations/{org}/workspaces | Create a workspace inside an organization.
[**delete_organization**](OrganizationsApi.md#delete_organization) | **DELETE** /v1/organizations/{org} | Delete an organization.
[**delete_organization_concept**](OrganizationsApi.md#delete_organization_concept) | **DELETE** /v1/organizations/{org}/concepts/{slug} | Delete a concept (admin+ only).
[**delete_organization_custom_role**](OrganizationsApi.md#delete_organization_custom_role) | **DELETE** /v1/organizations/{org}/roles/{roleId} | Delete a custom role (admin+ only).
[**delete_organization_logo**](OrganizationsApi.md#delete_organization_logo) | **DELETE** /v1/organizations/{org}/logo | Delete the organization logo.
[**get_organization**](OrganizationsApi.md#get_organization) | **GET** /v1/organizations/{org} | Fetch a single organization.
[**get_organization_concept**](OrganizationsApi.md#get_organization_concept) | **GET** /v1/organizations/{org}/concepts/{slug} | Fetch a concept.
[**list_my_organizations**](OrganizationsApi.md#list_my_organizations) | **GET** /v1/organizations | List the caller's organizations.
[**list_organization_audit_log**](OrganizationsApi.md#list_organization_audit_log) | **GET** /v1/organizations/{org}/audit-log | Read the organization audit log (admin / billing-admin only).
[**list_organization_concepts**](OrganizationsApi.md#list_organization_concepts) | **GET** /v1/organizations/{org}/concepts | List org-brain concepts (curated knowledge surfaced to agents).
[**list_organization_custom_roles**](OrganizationsApi.md#list_organization_custom_roles) | **GET** /v1/organizations/{org}/roles | List custom roles defined on the organization.
[**list_organization_invitations**](OrganizationsApi.md#list_organization_invitations) | **GET** /v1/organizations/{org}/invitations | List pending invitations for an organization.
[**list_organization_members**](OrganizationsApi.md#list_organization_members) | **GET** /v1/organizations/{org}/members | List members of an organization.
[**list_organization_workspaces**](OrganizationsApi.md#list_organization_workspaces) | **GET** /v1/organizations/{org}/workspaces | List workspaces in an organization.
[**remove_organization_member**](OrganizationsApi.md#remove_organization_member) | **DELETE** /v1/organizations/{org}/members/{memberId} | Remove a member from the organization.
[**resend_organization_invitation**](OrganizationsApi.md#resend_organization_invitation) | **POST** /v1/organizations/{org}/invitations/{invitationId}/resend | Revoke and reissue an invitation with a fresh token.
[**revoke_organization_invitation**](OrganizationsApi.md#revoke_organization_invitation) | **DELETE** /v1/organizations/{org}/invitations/{invitationId} | Revoke a pending invitation.
[**update_organization**](OrganizationsApi.md#update_organization) | **PATCH** /v1/organizations/{org} | Update organization metadata.
[**update_organization_concept**](OrganizationsApi.md#update_organization_concept) | **PATCH** /v1/organizations/{org}/concepts/{slug} | Update a concept (admin+ only).
[**update_organization_custom_role**](OrganizationsApi.md#update_organization_custom_role) | **PATCH** /v1/organizations/{org}/roles/{roleId} | Update a custom role (admin+ only).
[**update_organization_member**](OrganizationsApi.md#update_organization_member) | **PATCH** /v1/organizations/{org}/members/{memberId} | Update a member's role.
[**upload_organization_logo**](OrganizationsApi.md#upload_organization_logo) | **POST** /v1/organizations/{org}/logo | Upload (or replace) the organization logo. Multipart.



## accept_organization_invitation

> std::collections::HashMap<String, serde_json::Value> accept_organization_invitation(org, accept_organization_invitation_request)
Accept an invitation to this organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**accept_organization_invitation_request** | [**AcceptOrganizationInvitationRequest**](AcceptOrganizationInvitationRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_organization_member

> std::collections::HashMap<String, serde_json::Value> add_organization_member(org, add_organization_member_request)
Add a member directly (skips invitation flow).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**add_organization_member_request** | [**AddOrganizationMemberRequest**](AddOrganizationMemberRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_organization

> std::collections::HashMap<String, serde_json::Value> create_organization(create_organization_request)
Create an organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_organization_request** | [**CreateOrganizationRequest**](CreateOrganizationRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_organization_concept

> std::collections::HashMap<String, serde_json::Value> create_organization_concept(org, request_body)
Create an org-brain concept (admin+ only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_organization_custom_role

> std::collections::HashMap<String, serde_json::Value> create_organization_custom_role(org, request_body)
Create a custom role (admin+ only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_organization_invitation

> models::OrganizationInvitation create_organization_invitation(org, create_organization_invitation_request)
Invite a user to the organization.

Pending invitations count toward seat cap. Free-tier callers at the cap receive a `402` with billing-upgrade payload; paid-tier auto-scales the Stripe quantity. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**create_organization_invitation_request** | [**CreateOrganizationInvitationRequest**](CreateOrganizationInvitationRequest.md) |  | [required] |

### Return type

[**models::OrganizationInvitation**](OrganizationInvitation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_organization_workspace

> models::WorkspaceEnvelope create_organization_workspace(org, create_workspace_request)
Create a workspace inside an organization.

Requires the `OrgActionCreateWorkspace` action permission. Slug collisions auto-suffix (`-2`, `-3`, ...). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**create_workspace_request** | [**CreateWorkspaceRequest**](CreateWorkspaceRequest.md) |  | [required] |

### Return type

[**models::WorkspaceEnvelope**](WorkspaceEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_organization

> delete_organization(org)
Delete an organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** | Organization id or slug. | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_organization_concept

> delete_organization_concept(org, slug)
Delete a concept (admin+ only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**slug** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_organization_custom_role

> delete_organization_custom_role(org, role_id)
Delete a custom role (admin+ only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**role_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_organization_logo

> delete_organization_logo(org)
Delete the organization logo.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_organization

> models::OrganizationDetailLegacy get_organization(org)
Fetch a single organization.

**Wire format note:** response uses PascalCase keys (`ID`, `Name`, `Slug`, ...) — distinct from the rest of the SpatioAPI's camelCase convention. Documented as-is; a future cleanup will harmonize. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** | Organization id or slug. | [required] |

### Return type

[**models::OrganizationDetailLegacy**](OrganizationDetailLegacy.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_organization_concept

> std::collections::HashMap<String, serde_json::Value> get_organization_concept(org, slug)
Fetch a concept.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**slug** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_my_organizations

> models::OrganizationListResponse list_my_organizations()
List the caller's organizations.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::OrganizationListResponse**](OrganizationListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_organization_audit_log

> std::collections::HashMap<String, serde_json::Value> list_organization_audit_log(org, limit, cursor)
Read the organization audit log (admin / billing-admin only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**limit** | Option<**i32**> |  |  |
**cursor** | Option<**String**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_organization_concepts

> std::collections::HashMap<String, serde_json::Value> list_organization_concepts(org)
List org-brain concepts (curated knowledge surfaced to agents).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_organization_custom_roles

> std::collections::HashMap<String, serde_json::Value> list_organization_custom_roles(org)
List custom roles defined on the organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_organization_invitations

> models::OrganizationInvitationListResponse list_organization_invitations(org)
List pending invitations for an organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |

### Return type

[**models::OrganizationInvitationListResponse**](OrganizationInvitationListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_organization_members

> models::OrganizationMemberListResponse list_organization_members(org)
List members of an organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |

### Return type

[**models::OrganizationMemberListResponse**](OrganizationMemberListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_organization_workspaces

> models::WorkspaceListResponse list_organization_workspaces(org)
List workspaces in an organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |

### Return type

[**models::WorkspaceListResponse**](WorkspaceListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_organization_member

> remove_organization_member(org, member_id)
Remove a member from the organization.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**member_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## resend_organization_invitation

> models::OrganizationInvitation resend_organization_invitation(org, invitation_id)
Revoke and reissue an invitation with a fresh token.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**invitation_id** | **String** |  | [required] |

### Return type

[**models::OrganizationInvitation**](OrganizationInvitation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## revoke_organization_invitation

> revoke_organization_invitation(org, invitation_id)
Revoke a pending invitation.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**invitation_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_organization

> std::collections::HashMap<String, serde_json::Value> update_organization(org, update_organization_request)
Update organization metadata.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** | Organization id or slug. | [required] |
**update_organization_request** | [**UpdateOrganizationRequest**](UpdateOrganizationRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_organization_concept

> std::collections::HashMap<String, serde_json::Value> update_organization_concept(org, slug, request_body)
Update a concept (admin+ only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**slug** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_organization_custom_role

> std::collections::HashMap<String, serde_json::Value> update_organization_custom_role(org, role_id, request_body)
Update a custom role (admin+ only).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**role_id** | **String** |  | [required] |
**request_body** | [**std::collections::HashMap<String, serde_json::Value>**](SerdeJson__Value.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_organization_member

> std::collections::HashMap<String, serde_json::Value> update_organization_member(org, member_id, update_organization_member_request)
Update a member's role.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**member_id** | **String** |  | [required] |
**update_organization_member_request** | [**UpdateOrganizationMemberRequest**](UpdateOrganizationMemberRequest.md) |  | [required] |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_organization_logo

> std::collections::HashMap<String, serde_json::Value> upload_organization_logo(org, file)
Upload (or replace) the organization logo. Multipart.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**org** | **String** |  | [required] |
**file** | Option<**std::path::PathBuf**> |  |  |

### Return type

[**std::collections::HashMap<String, serde_json::Value>**](serde_json::Value.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

