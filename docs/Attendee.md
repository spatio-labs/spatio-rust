# Attendee

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **String** |  | 
**name** | Option<**String**> |  | [optional]
**status** | [**models::AttendeeStatus**](AttendeeStatus.md) |  | 
**role** | [**models::AttendeeRole**](AttendeeRole.md) |  | 
**optional** | **bool** | Legacy boolean — superseded by `role` (`role: optional` carries the same signal). Kept on the wire for client compatibility.  | 
**comment** | Option<**String**> |  | [optional]
**additional_guests** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


