## Failed Vehicle Lock - `A002`

Triggered when the vehicle lock fails to engage due to excessive
torque applied to the connector.

### EVSE Display Requirements

Prompt the user to unplug the connector, wait 10s, and reattach
the connector. Further instruct the user that the cable connector
should be seated fully to ensure the vehicle lock engages successfully.

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
		"vendorErrorCode": "A002"
    }
]
```
