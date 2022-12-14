## Code Format

Error codes defined within this specification are mapped to a 16-bit hexadecimal encoded string
in network order:

The first byte (left pair) is the *prefix*:

- Codes prefixed in the range `A0` to `AF` (inclusive) are *user actionable*, and potentially
result from *user error*.
- Codes prefixed in the range `F0` to `FF` (inclusive) are **safety** related, and are not
actionable by the end user.

The second byte (right pair) is the *code*, occupying the range `00` to `FF` (inclusive).

Allocation of codes will begin with `A000` and `F000`.

## EVSE Display Requirements

Each code will define a generic requirement for what information **shall** be displayed
to the customer. In cases where a CPO has custom screen flows, these will be
provided by the CPO directly.

These requirements are waived for devices where no display is present.

## Status Notification Conventions

1. The `info` field shall contain informative values, such as relevant sensor readings,
recorded at the time of the event where available.
2. The `timestamp` field is  **required**. This value **must** be in ISO8601 format.
UTC is the **only** acceptable timezone. Example: `2022-06-10T14:51:17Z`
3. The `vendorId` is `com.evgo.mrec`

## Compound Error Codes

Given the potential for concurrent, or complex, failure modes to exist the following
shall govern the transmission of data in such an event. When concurrent error states
exist, the details **shall** be sent such that individual values as required in the
spec are sent as Comma Separated Values within the `info` and `vendorErrorCode` fields.

Mapping is such that the N-th value present in `info` is the instrumentation measurement
corresponding to the N-th value present in `vendorErrorCode`. A reference example follows
using codes [`F001`](./def/f/prox-low.md) and [`F003`](./def/f/pilot-low.md):

Example:
```json
[
    2,
    "12345",
    "StatusNotification",
    {
		"connectorId": 1,
		"errorCode": "OtherError",
		"info": "1.11,5.00",
		"status": "Finishing",
		"timestamp": "2022-06-10T14:51:17Z",
		"vendorId": "com.evgo.mrec",
		"vendorErrorCode": "F001,F003"
    }
]
```
