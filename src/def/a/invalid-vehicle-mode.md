## Invalid Vehicle Mode - `A003`

Triggered when the vehicle is in an invalid mode for charging, for
example:

- The shift selection is some value other than "Park"
- The vehicle is "ON"
- The vehicle is ready to drive

### EVSE Display Requirements

The HMI shall inform the user that the vehicle must be OFF and in Park
in order to charge.

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
		"vendorErrorCode": "A003"
    }
]
```
