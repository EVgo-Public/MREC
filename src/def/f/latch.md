## Broken Latch - `F004`

Triggered and sent to the CPO in the event that the connector latch of the EVSE
is broken as described in SAE J1772 6.5.9, and the impacted EVSE is capable of
detecting the fault.

When the fault occurs, proximity voltage can be observed entering the range 1.23V
to 1.82V without having first entered the 2.38V to 3.16V range prior to a charge
starting.

### EVSE Display Requirements

Warn the user the connector latch may be damaged, and note that the CPO has been
notified.

If contacting Customer Service, reference error code: `F004`.

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
		"vendorErrorCode": "F004"
    }
]
```
