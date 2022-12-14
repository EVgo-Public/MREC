## Proximity Voltage: High - `F000`

Triggered and sent to the CPO in the event that the proximity signal is out of range
on the **high** side. This occurs when the proximity signal is above 1.82VDC during 
active charging.

In the `StatusNotification.req` use the `info` field to provide the *measured* proximity
value at the time of failure. The units **shall** be `VDC`.

### EVSE Display Requirements

Prompt the user that an error has occured, and provide instruction to try again.

The instruction to try again **should** suggest confirming a properly seated connector.

If contacting Customer Service, reference error code: `F000`.

### Sample Message

```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "2.00",
		"status": "Finishing",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F000"
    }
]
```
