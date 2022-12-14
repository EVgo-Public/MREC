## Cable Cut - `F010`

Triggered and sent to the CPO in the event that both temperature sensors in the
charging cable simultaneously read at their maximum value. This behavior is seen
when the charging cable has been cut.

### EVSE Display Requirements

Display the general Error screen, and note that the CPO has been notified.

If contacting Customer Service, reference error code: `F010`.

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
		"vendorErrorCode": "F010"
    }
]
```
