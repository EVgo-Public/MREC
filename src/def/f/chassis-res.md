## Chassis Resistance: Low - `F006`

Triggered and sent to the CPO in the event an Isolation Monitoring Device
trips due to low resistance to the chassis during active charging. This occurs 
when the measured resistance from V+ or V- to chassis is below 100Ω/V, 
where V is the output voltage.

In the `StatusNotification.req` use the `info` field to provide the *measured*
resistance value to the chassis at the time of failure. The units **shall** be `kΩ`.
Omit if no measurement is available.

### EVSE Display Requirements

Display the general Error screen, and note that the CPO has been notified.

If contacting Customer Service, reference error code: `F006`.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "20",
		"status": "Faulted",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F006"
    }
]
```
