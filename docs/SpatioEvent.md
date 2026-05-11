# SpatioEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**title** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**start_time** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**end_time** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**all_day** | **bool** |  | 
**location** | Option<**String**> |  | [optional]
**location_details** | Option<**std::collections::HashMap<String, String>**> | Free-form key/value (lat, lng, room, etc.). | [optional]
**organizer** | Option<**String**> | Organizer email. | [optional]
**attendees** | Option<[**Vec<models::Attendee>**](Attendee.md)> |  | [optional]
**recurrence_rule** | Option<**String**> | RFC 5545 RRULE. | [optional]
**recurrence_id** | Option<**String**> | Set on instances of a recurring series. | [optional]
**original_start** | Option<**chrono::DateTime<chrono::FixedOffset>**> | Original start of a moved recurring instance. | [optional]
**status** | **String** | Provider-mapped event status. Free-form string — common values are `confirmed`, `tentative`, `cancelled`, `needs_action`, and the empty string when the provider doesn't populate it. Not enumerated strictly because providers add custom values and the platform passes them through verbatim.  | 
**visibility** | **String** | Free-form visibility string. Common values: `public`, `private`, `confidential`, plus empty when unset.  | 
**busy** | **bool** | Whether this event marks the time as busy or free. | 
**reminders** | Option<[**Vec<models::Reminder>**](Reminder.md)> |  | [optional]
**travel_time_minutes** | Option<**i32**> | Apple Calendar's local-only travel buffer. Stored on the cached row but not synced to providers that don't model it.  | [optional]
**categories** | Option<**Vec<String>**> |  | [optional]
**color** | Option<**String**> |  | [optional]
**user_id** | Option<**String**> |  | [optional]
**account_id** | **String** |  | 
**provider** | Option<**String**> | Standardized provider id (e.g. `google-calendar`, `native-calendar`). Mirrors `provider_id` — both are populated on writes; clients should prefer `provider`.  | [optional]
**provider_id** | **String** | Legacy alias of `provider`. | 
**provider_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Provider-specific extras. | [optional]
**created_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**updated_at** | **chrono::DateTime<chrono::FixedOffset>** |  | 
**deleted_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**synced_at** | Option<**chrono::DateTime<chrono::FixedOffset>**> |  | [optional]
**conference_data** | Option<[**models::ConferenceData**](ConferenceData.md)> |  | [optional]
**attachments** | Option<[**Vec<models::Attachment>**](Attachment.md)> |  | [optional]
**url** | Option<**String**> |  | [optional]
**etag** | Option<**String**> |  | [optional]
**sequence** | Option<**i32**> |  | [optional]
**custom_data** | Option<**std::collections::HashMap<String, String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


