# CreateEventRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**calendar_id** | Option<**String**> | Specific calendar within the account; omit for the default. | [optional]
**event** | [**models::SpatioEvent**](SpatioEvent.md) |  | 
**send_updates** | Option<**SendUpdates**> | Notification policy passed through to the provider. (enum: all, externalOnly, none) | [optional]
**conference_type** | Option<**String**> | When set, the platform will auto-attach a conference link of the matching type (`spatio`, `meet`, `zoom`, `teams`).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


