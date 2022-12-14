## Authorization Timeout - `A000`

Triggered when the *user* plugs in but fails to authorize a
charging session prior to the connection timeout between the
vehicle and EVSE.

### EVSE Display Requirements

The HMI shall inform the user that the delay between plug-in
and authorization exceeded the timeout, and prompt the user
to try again.

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
		"vendorErrorCode": "A000"
    }
]
```
