## Proximity Voltage: Low - `F001`

Triggered and sent to the CPO in the event that the proximity signal is out of range
on the **low** side. This occurs when the proximity signal is below 1.23VDC during
active charging.

In the `StatusNotification.req` use the `info` field to provide the *measured* proximity
value at the time of failure. The units **shall** be `VDC`.

### EVSE Display Requirement

Prompt the user that an error has occured, and provide instruction to try again.

The instruction to try again **should** suggest confirming a properly seated connector.

If contacting Customer Service, reference error code: `F001`.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "1.11",
		"status": "Finishing",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F001"
    }
]
```
