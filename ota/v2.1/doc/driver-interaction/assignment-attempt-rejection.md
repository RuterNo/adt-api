# [v2.1](../../README.md) / [Driver interaction](README.md) / Assignment attempt rejection 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/di/assignment_attempt_rejection/block```  | ```false``` | ```0```

# AssignmentAttemptRejection Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/driver-interaction/assignment-attempt-rejection.json
```

Describes a negative result from the back-office of an attempt to sign on or off a block from MADT or another GUI


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                    |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [assignment-attempt-rejection.json](../../schema/driver-interaction/assignment-attempt-rejection.json "open original schema") |

## AssignmentAttemptRejection Type

`object` ([AssignmentAttemptRejection](assignment-attempt-rejection.md))

## AssignmentAttemptRejection Examples

```json
{
  "fromDateTime": "2017-10-31T12:45:50Z",
  "blockRef": "10023",
  "result": "NOT_GRANTED",
  "errorText": "Already signed on in another vehicle"
}
```

# AssignmentAttemptRejection Properties

| Property                      | Type     | Required | Nullable       | Defined by                                                                                                                                  |
| :---------------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| [fromDateTime](#fromdatetime) | `string` | Required | cannot be null | [AssignmentAttemptRejection](assignment-attempt-rejection-properties-fromdatetime.md "\#/properties/fromDateTime#/properties/fromDateTime") |
| [blockRef](#blockref)         | `string` | Optional | cannot be null | [AssignmentAttemptRejection](assignment-attempt-rejection-properties-blockref.md "\#/properties/blockRef#/properties/blockRef")             |
| [result](#result)             | `string` | Required | cannot be null | [AssignmentAttemptRejection](assignment-attempt-rejection-properties-result.md "\#/properties/result#/properties/result")                   |
| [errorText](#errortext)       | `string` | Optional | cannot be null | [AssignmentAttemptRejection](assignment-attempt-rejection-properties-errortext.md "\#/properties/errorText#/properties/errorText")          |
| Additional Properties         | Any      | Optional | can be null    |                                                                                                                                             |

## fromDateTime

Time from which the sign on/off was supposed to apply. ISO 8601, UTC


`fromDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttemptRejection](assignment-attempt-rejection-properties-fromdatetime.md "\#/properties/fromDateTime#/properties/fromDateTime")

### fromDateTime Type

`string`

## blockRef

Optional. Not provided for sign off. Otherwise the Block identifier.


`blockRef`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttemptRejection](assignment-attempt-rejection-properties-blockref.md "\#/properties/blockRef#/properties/blockRef")

### blockRef Type

`string`

## result

Possible values listed in examples


`result`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttemptRejection](assignment-attempt-rejection-properties-result.md "\#/properties/result#/properties/result")

### result Type

`string`

### result Examples

```json
"INTERNAL_ERROR"
```

```json
"TIMEOUT"
```

```json
"SERVICE_CLOSED"
```

```json
"NOT_SUCCEDED"
```

```json
"NOT_GRANTED"
```

```json
"NOT_SUPPORTED"
```

```json
"NOT_UNDERSTOOD"
```

## errorText

Optional. Only provided if there is an error text.


`errorText`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttemptRejection](assignment-attempt-rejection-properties-errortext.md "\#/properties/errorText#/properties/errorText")

### errorText Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
