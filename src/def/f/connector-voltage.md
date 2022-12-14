## Connector Voltage: High - `F008`

Triggered and sent to the CPO in the event EVSE output voltage is detected above
60VDC before charging begins, or after charging ends.

In the `StatusNotification.req` use the `info` field to provide the *measured*
output voltage on the connector at the time of failure. The units **shall** be `VDC`.

### EVSE Display Requirements

Display the general Error screen, and note that the CPO has been notified.

If contacting Customer Service, reference error code: `F008`.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "70",
		"status": "Faulted",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F008"
    }
]
```
