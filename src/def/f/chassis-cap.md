## Chassis Capacitance: High - `F007`

Triggered and sent to the CPO in the event an Isolation Monitoring Device
trips due to high capacitance to the chassis during active charging. This 
occurs when the measured capacitance from V+ or V- to chassis is above 5μF.

In the `StatusNotification.req` use the `info` field to provide the *measured*
capacitance value to the chassis at the time of failure. The units **shall** be `μF`.
Omit if no measurement is available.

### EVSE Display Requirements

Display the general Error screen, and note that the CPO has been notified.

If contacting Customer Service, reference error code: `F007`.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "10",
		"status": "Faulted",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F007"
    }
]
```
