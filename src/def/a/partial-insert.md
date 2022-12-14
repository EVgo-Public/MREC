## Partial Insertion - `A001`

Triggered when the cable latch is raised due to incomplete
insertion into the vehicle charging port.

### EVSE Display Requirements

Prompt the user to unplug the connector, wait 10s, and reattach
the connector. Further instruct the user that the cable connector
must be seated fully to ensure the cable latch is completely closed.

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
		"vendorErrorCode": "A001"
    }
]
```
