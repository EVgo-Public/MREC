## Minimum Required Error Codes

This document defines **mandatory** error codes necessary for responsible operation
of EV charging infrastructure. Transport **shall** occur over OCPP 1.6J, and
**shall** leverage fields defined within the `StatusNotification.req`.

The substance of the messages defined herein are critical, and the format is that
suggested by EVgo. If all conditions, including transmitted data, of a defined
code are present within a manufacturer's own error codes it is sufficient for a
manufacturer to indicate which internal code maps to the corresponding MREC code.

## Motivation

To reduce MTTR of customer-facing charging problems through the improvement, and unification, of EVSE error codes.
