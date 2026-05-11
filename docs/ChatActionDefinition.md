# ChatActionDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**platform** | **String** |  | 
**category** | Option<**String**> | Common values: `read`, `write`, `delete`, `manage`, `sync`. | [optional]
**input_type** | Option<**String**> |  | [optional]
**output_type** | Option<**String**> |  | [optional]
**scopes** | Option<**Vec<String>**> | `null` when no scopes are declared (Go nil-slice). | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


