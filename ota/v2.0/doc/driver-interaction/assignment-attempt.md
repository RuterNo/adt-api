# [v2.0](../../README.md) / [Driver interaction](README.md) / Assignment attempt 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/di/assignment_attempt/block```  | ```true``` | ```1```

# AssignmentAttempt Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/driver-interaction/assignment-attempt.json
```

Describes an attempt to sign on or off a block from MADT, another GUI or from the PTO backoffice. The result of this request will be confirmed by the PTA backoffice and the results presented either on the topic ruter/{PTO}/{vehicleID}/oi/current\_ block/state or the topic ruter/{PTO}/{vehicleID}/di/assignment_attempt_rejection/block.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | --------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [assignment-attempt.json](../../schema/driver-interaction/assignment-attempt.json "open original schema") |

## AssignmentAttempt Type

`object` ([AssignmentAttempt](assignment-attempt.md))

## AssignmentAttempt Examples

```json
{
  "fromDateTime": "2017-10-31T12:45:00Z",
  "vehicleRef": "1HGCM82633A004352",
  "blockRef": "10023",
  "apiVersion": "v2",
  "assignmentType": "SIGNON",
  "assignmentCode": "PLANNED"
}
```

# AssignmentAttempt Properties

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                                     |
| :-------------------------------- | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------- |
| [fromDateTime](#fromdatetime)     | `string` | Required | cannot be null | [AssignmentAttempt](assignment-attempt-properties-fromdatetime.md "\#/properties/fromDateTime#/properties/fromDateTime")       |
| [vehicleRef](#vehicleref)         | `string` | Required | cannot be null | [AssignmentAttempt](assignment-attempt-properties-vehicleref.md "\#/properties/vehicleRef#/properties/vehicleRef")             |
| [blockRef](#blockref)             | `string` | Optional | cannot be null | [AssignmentAttempt](assignment-attempt-properties-blockref.md "\#/properties/blockRef#/properties/blockRef")                   |
| [apiVersion](#apiversion)         | `string` | Required | cannot be null | [AssignmentAttempt](assignment-attempt-properties-apiversion.md "\#/properties/apiVersion#/properties/apiVersion")             |
| [assignmentType](#assignmenttype) | `string` | Required | cannot be null | [AssignmentAttempt](assignment-attempt-properties-assignmenttype.md "\#/properties/assignmentType#/properties/assignmentType") |
| [assignmentCode](#assignmentcode) | `string` | Required | cannot be null | [AssignmentAttempt](assignment-attempt-properties-assignmentcode.md "\#/properties/assignmentCode#/properties/assignmentCode") |
| Additional Properties             | Any      | Optional | can be null    |                                                                                                                                |

## fromDateTime

Time, according to sheduled departure, from which the sign on/off applies. ISO 8601, UTC. Eg. departure time of block, journey (partial servicing of block) or call on Journey (partial servicing of journey)


`fromDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttempt](assignment-attempt-properties-fromdatetime.md "\#/properties/fromDateTime#/properties/fromDateTime")

### fromDateTime Type

`string`

## vehicleRef

ID of the vehicle/vessel.


`vehicleRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttempt](assignment-attempt-properties-vehicleref.md "\#/properties/vehicleRef#/properties/vehicleRef")

### vehicleRef Type

`string`

## blockRef

Optional. Not provided for sign off. Otherwise the Block identifier to be signed on. 


`blockRef`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttempt](assignment-attempt-properties-blockref.md "\#/properties/blockRef#/properties/blockRef")

### blockRef Type

`string`

## apiVersion

'v2' for ADT v2.x. Attribute in use by Ruter only. Not part of ITxPT specification.


`apiVersion`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttempt](assignment-attempt-properties-apiversion.md "\#/properties/apiVersion#/properties/apiVersion")

### apiVersion Type

`string`

## assignmentType

Attribute in use by Ruter only. Not part of ITxPT specification.


`assignmentType`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttempt](assignment-attempt-properties-assignmenttype.md "\#/properties/assignmentType#/properties/assignmentType")

### assignmentType Type

`string`

### assignmentType Examples

```json
"SIGNON"
```

```json
"SIGNOFF"
```

## assignmentCode

Attribute in use by Ruter only. Not part of ITxPT specification.


`assignmentCode`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AssignmentAttempt](assignment-attempt-properties-assignmentcode.md "\#/properties/assignmentCode#/properties/assignmentCode")

### assignmentCode Type

`string`

### assignmentCode Examples

```json
"PLANNED"
```

```json
"EXTRA"
```

```json
"SHORTENING"
```

```json
"CANCELED"
```

```json
"BREAKDOWN"
```

```json
"FINISHED"
```

```json
"REPLACEMENT"
```

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
