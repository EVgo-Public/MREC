## Pilot Voltage: High - `F002`

Triggered and sent to the CPO in the event that the pilot signal is out of range
on the **high** side. This occurs when the pilot signal is above 6.53VDC during
active charging.

In the `StatusNotification.req` use the `info` field to provide the *measured* proximity
value at the time of failure. The units **shall** be `VDC`.

### EVSE Display Requirements

Prompt the user that an error has occured, and provide instruction to try again.

The instruction to try again **should** suggest confirming a properly seated connector.

If contacting Customer Service, reference error code: `F002`.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "7.00",
		"status": "Finishing",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F002"
    }
]
```
