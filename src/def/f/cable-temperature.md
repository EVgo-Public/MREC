## Cable Over Temperature - `F009`

Triggered and sent to the CPO in the event that any temperature sensor in the
charging cable reads at or above the max temperature.

In the `StatusNotification.req` use the `info` field to provide the *measured*
temperature value of the thermistor at the time of failure. The units **shall**
be `degrees C`. Omit if no measurement is available.

### EVSE Display Requirements

Display the general Error screen, and note that the CPO has been notified.

If contacting Customer Service, reference error code: `F009`.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "96",
		"status": "Faulted",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F009"
    }
]
```
