## Emergency Stop Pressed - `A004`

Triggered when the Emergency Stop button is pressed on the EVSE outside
of an active charging session. While OCPP 1.6J defines pressing the
Emergency Stop button as a Stop Reason, there is no fixed code to inform
the CPO when the button is pressed outside of a charging session.

### EVSE Display Requirements

Prompt the user to twist, or otherwise manipulate, the Emergency Stop
button as required to disengage the button.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 0,
		"errorCode": "OtherError",
		"info": "",
		"status": "Faulted",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "A004"
    }
]
```
