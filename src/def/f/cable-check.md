## Failed Cable Check - `F005`

Triggered and sent to the CPO in the event that isolation failure occurs during
the cable check phase.

This fault occurs between Authorization and Preparing.

### EVSE Display Requirements

Display the general Error screen, and note that the CPO has been notified.

If contacting Customer Service, reference error code: `F005`.

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
		"vendorErrorCode": "F005"
    }
]
```
