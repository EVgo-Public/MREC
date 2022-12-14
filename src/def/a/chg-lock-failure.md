## Failed Charger Lock - `A005`

Triggered when the charger connector lock fails to engage due to the
CHAdeMO connector not being fully inserted into the socket, or the CHAdeMO
connector lock is not operationl. Note this is only required to be supported
for systems that include a CHAdeMO connector.

### EVSE Display Requirements

Prompt the user to unplug the connector, wait 10s, and reattach
the connector. Further instruct the user that the cable connector
should be seated fully to ensure the charger lock engages successfully.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "",
		"status": "Faulted",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "A005"
    }
]
```
