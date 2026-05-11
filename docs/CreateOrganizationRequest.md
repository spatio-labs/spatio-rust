# CreateOrganizationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**slug** | Option<**String**> | Auto-generated from `name` if omitted. Slug collisions are auto-suffixed with `-2`, `-3`, etc.  | [optional]
**description** | Option<**String**> |  | [optional]
**logo_url** | Option<**String**> |  | [optional]
**create_default_workspace** | Option<**bool**> | `true` (default) creates a default workspace alongside the org. | [optional]
**default_workspace_name** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


