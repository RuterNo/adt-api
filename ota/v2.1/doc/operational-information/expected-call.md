# [v2.1](../../README.md) / [Operational information](README.md) / Expected call 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/expected_call```  | ```true``` | ```1```

# ExpectedCall Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json
```

The topic should provide a consistent set of current information describing the vehicle’s current, previous and next stop(s) including estimated times, observed times and additional information helping the driver to adhere to the operation control centre’s current plan for this vehicle. The topic is focused on the stop that the vehicle is standing at or will arrive to next in the case that the vehicle is between stops. The topic should be blanked (provided as a retained message with a zero-byte payload) if the vehicle has left the last stop and if it is not known what the next vehicle journey will be.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                           |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------------------------------- |
| Can be instantiated | Yes        | Unknown status | No           | Forbidden         | Allowed               | none                | [expected-call.json](../../schema/operational-information/expected-call.json "open original schema") |

## ExpectedCall Type

`object` ([ExpectedCall](expected-call.md))

## ExpectedCall Examples

```json
{
  "updatedAtDateTime": "2017-10-31T12:45:50Z",
  "vehicleJourneyRef": "9015001098702345",
  "callSequenceNumber": 3,
  "pointRef": "9025001000012345",
  "tariffZone": {
    "ref": "225",
    "number": "2V"
  },
  "atStop": true,
  "observedTimeOfArrival": "2017-10-31T12:45:50Z",
  "estimatedTimeOfDeparture": "2017-10-31T12:46:30Z",
  "serviceDeviation": 30,
  "holdReason": "CONNECTION_PROTECTION",
  "holdUntil": "2017-10-31T12:46:30Z",
  "restriction": "NO_ALIGHTING",
  "previousCall": {
    "callSequenceNumber": 2,
    "pointRef": "9025001000012333",
    "observedTimeOfArrival": "2017-10-31T12:43:50Z",
    "observedTimeOfDeparture": "2017-10-31T12:44:32Z"
  },
  "laterCalls": [
    {
      "callSequenceNumber": 4,
      "pointRef": "9025001000012377",
      "estimatedTimeOfArrival": "2017-10-31T12:48:23Z",
      "estimatedTimeOfDeparture": "2017-10-31T12:49:10Z",
      "restriction": "NO_BOARDING"
    },
    {
      "callSequenceNumber": 5,
      "pointRef": "9025001000012332",
      "estimatedTimeOfArrival": "2017-10-31T12:53:50Z",
      "estimatedTimeOfDeparture": "2017-10-31T12:54:20Z"
    }
  ]
}
```

# ExpectedCall Properties

| Property                                              | Type      | Required | Nullable       | Defined by                                                                                                                                        |
| :---------------------------------------------------- | :-------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| [updatedAtDateTime](#updatedatdatetime)               | `string`  | Required | cannot be null | [ExpectedCall](expected-call-properties-updatedatdatetime.md "#/properties/updatedAtDateTime#/properties/updatedAtDateTime")                      |
| [vehicleJourneyRef](#vehiclejourneyref)               | `string`  | Required | cannot be null | [ExpectedCall](expected-call-properties-vehiclejourneyref.md "#/properties/vehicleJourneyRef#/properties/vehicleJourneyRef")                      |
| [callSequenceNumber](#callsequencenumber)             | `number`  | Required | cannot be null | [ExpectedCall](expected-call-properties-callsequencenumber.md "#/properties/callSequenceNumber#/properties/callSequenceNumber")                   |
| [pointRef](#pointref)                                 | `string`  | Required | cannot be null | [ExpectedCall](expected-call-properties-pointref.md "#/properties/pointRef#/properties/pointRef")                                                 |
| [tariffZone](#tariffzone)                             | `object`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-tariff-zone-info.md "#/properties/tariffZone#/properties/tariffZone")                                     |
| [atStop](#atstop)                                     | `boolean` | Required | cannot be null | [ExpectedCall](expected-call-properties-atstop.md "#/properties/atStop#/properties/atStop")                                                       |
| [estimatedTimeOfArrival](#estimatedtimeofarrival)     | `string`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-estimatedtimeofarrival.md "#/properties/estimatedTimeOfArrival#/properties/estimatedTimeOfArrival")       |
| [observedTimeOfArrival](#observedtimeofarrival)       | `string`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-observedtimeofarrival.md "#/properties/observedTimeOfArrival#/properties/observedTimeOfArrival")          |
| [estimatedTimeOfDeparture](#estimatedtimeofdeparture) | `string`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-estimatedtimeofdeparture.md "#/properties/estimatedTimeOfDeparture#/properties/estimatedTimeOfDeparture") |
| [serviceDeviation](#servicedeviation)                 | `number`  | Required | cannot be null | [ExpectedCall](expected-call-properties-servicedeviation.md "#/properties/serviceDeviation#/properties/serviceDeviation")                         |
| [holdReason](#holdreason)                             | `string`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-holdreason.md "#/properties/holdReason#/properties/holdReason")                                           |
| [holdUntil](#holduntil)                               | `string`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-holduntil.md "#/properties/holdUntil#/properties/holdUntil")                                              |
| [restriction](#restriction)                           | `string`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-restriction.md "#/properties/restriction#/properties/restriction")                                        |
| [previousCall](#previouscall)                         | `object`  | Optional | cannot be null | [ExpectedCall](expected-call-properties-call.md "#/properties/previousCall#/properties/previousCall")                                             |
| [laterCalls](#latercalls)                             | `array`   | Optional | cannot be null | [ExpectedCall](expected-call-properties-latercalls.md "#/properties/laterCalls#/properties/laterCalls")                                           |
| Additional Properties                                 | Any       | Optional | can be null    |                                                                                                                                                   |

## updatedAtDateTime

Time when last updated. ISO 8601, UTC.

`updatedAtDateTime`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-updatedatdatetime.md "#/properties/updatedAtDateTime#/properties/updatedAtDateTime")

### updatedAtDateTime Type

`string`

## vehicleJourneyRef

A Vehicle Journey identifier.

`vehicleJourneyRef`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-vehiclejourneyref.md "#/properties/vehicleJourneyRef#/properties/vehicleJourneyRef")

### vehicleJourneyRef Type

`string`

## callSequenceNumber

Order number of stop in journey pattern.

`callSequenceNumber`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-callsequencenumber.md "#/properties/callSequenceNumber#/properties/callSequenceNumber")

### callSequenceNumber Type

`number`

## pointRef

A stop identifier.

`pointRef`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-pointref.md "#/properties/pointRef#/properties/pointRef")

### pointRef Type

`string`

## tariffZone

Optional. The tariff zone of the stop.

`tariffZone`

*   is optional

*   Type: `object` ([Tariff Zone Info](expected-call-properties-tariff-zone-info.md))

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-tariff-zone-info.md "#/properties/tariffZone#/properties/tariffZone")

### tariffZone Type

`object` ([Tariff Zone Info](expected-call-properties-tariff-zone-info.md))

## atStop

True if vehicle is standing at (has arrived to) the stop. False when between stops.

`atStop`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-atstop.md "#/properties/atStop#/properties/atStop")

### atStop Type

`boolean`

### atStop Examples

```json
"true"
```

```json
"false"
```

## estimatedTimeOfArrival

Optional. Only provided if the vehicle has not arrived at this stop. ISO 8601, UTC.

`estimatedTimeOfArrival`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-estimatedtimeofarrival.md "#/properties/estimatedTimeOfArrival#/properties/estimatedTimeOfArrival")

### estimatedTimeOfArrival Type

`string`

## observedTimeOfArrival

Optional. Only provided if the vehicle has arrived at this stop. ISO 8601, UTC.

`observedTimeOfArrival`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-observedtimeofarrival.md "#/properties/observedTimeOfArrival#/properties/observedTimeOfArrival")

### observedTimeOfArrival Type

`string`

## estimatedTimeOfDeparture

Optional. Usually not provided for the last call of the journey. ISO 8601, UTC.

`estimatedTimeOfDeparture`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-estimatedtimeofdeparture.md "#/properties/estimatedTimeOfDeparture#/properties/estimatedTimeOfDeparture")

### estimatedTimeOfDeparture Type

`string`

## serviceDeviation

Value related to timetable or regularity depending on operation mode. A negative value indicates the number of seconds the vehicle journey is behind optimal time and a positive value indicates the number of seconds it is ahead of optimal time.

`serviceDeviation`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-servicedeviation.md "#/properties/serviceDeviation#/properties/serviceDeviation")

### serviceDeviation Type

`number`

## holdReason

Optional. Only provided if vehicle should hold. Describes the reason why the driver should hold at this stop. Possible values in examples.

`holdReason`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-holdreason.md "#/properties/holdReason#/properties/holdReason")

### holdReason Type

`string`

### holdReason Examples

```json
"CONNECTION_PROTECTION"
```

```json
"TIMING_POINT"
```

```json
"DRIVER_CHANGE"
```

## holdUntil

Optional. Only provided if vehicle should hold. Time of earliest permitted departure. ISO 8601, UTC.

`holdUntil`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-holduntil.md "#/properties/holdUntil#/properties/holdUntil")

### holdUntil Type

`string`

## restriction

Optional. Only provided if boarding or alighting restriction applies based on a combination of planned restrictions and partial journey cancellations. Possible values in examples.

`restriction`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-restriction.md "#/properties/restriction#/properties/restriction")

### restriction Type

`string`

### restriction Examples

```json
"NO_BOARDING"
```

```json
"NO_ALIGHTING"
```

```json
"NO_STOP"
```

## previousCall

Optional. Describes the call to the stop immediately preceding the expected call. Only provided if there is at least one call in the journey before the expected call.

`previousCall`

*   is optional

*   Type: `object` ([Call](expected-call-properties-call.md))

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-call.md "#/properties/previousCall#/properties/previousCall")

### previousCall Type

`object` ([Call](expected-call-properties-call.md))

## laterCalls

Optional. Only provided if there are any calls in the journey after the expected call. Describes a configured number of calls that follow in sequence after the expected call. Note that the first item in the list represents the "next stop" only when the vehicle is standing at a stop. If the vehicle is between stops then the first item represents the first stop after the next stop. The configured max number of later Calls to be expected should be provided in configValue01 for this topic under topic tobs/mi/provider_clients//provided_topics.

`laterCalls`

*   is optional

*   Type: unknown\[]

*   cannot be null

*   defined in: [ExpectedCall](expected-call-properties-latercalls.md "#/properties/laterCalls#/properties/laterCalls")

### laterCalls Type

unknown\[]

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema

# ExpectedCall Definitions

## Definitions group call

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call"}
```

| Property                                                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                         |
| :------------------------------------------------------ | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [callSequenceNumber](#callsequencenumber-1)             | `number` | Required | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-callsequencenumber.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/callSequenceNumber")             |
| [pointRef](#pointref-1)                                 | `string` | Required | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-pointref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/pointRef")                                 |
| [estimatedTimeOfArrival](#estimatedtimeofarrival-1)     | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofarrival.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfArrival")     |
| [observedTimeOfArrival](#observedtimeofarrival-1)       | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-observedtimeofarrival.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfArrival")       |
| [estimatedTimeOfDeparture](#estimatedtimeofdeparture-1) | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofdeparture.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfDeparture") |
| [observedTimeOfDeparture](#observedtimeofdeparture)     | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-observedtimeofdeparture.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfDeparture")   |
| [restriction](#restriction-1)                           | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-restriction.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/restriction")                           |

### callSequenceNumber

Order number of stop in journey pattern. (One-based list).

`callSequenceNumber`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-call-properties-callsequencenumber.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/callSequenceNumber")

#### callSequenceNumber Type

`number`

### pointRef

A stop identifier.

`pointRef`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-call-properties-pointref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/pointRef")

#### pointRef Type

`string`

### estimatedTimeOfArrival

Optional. Only provided if the vehicle has not arrived at this stop. ISO 8601, UTC.

`estimatedTimeOfArrival`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofarrival.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfArrival")

#### estimatedTimeOfArrival Type

`string`

### observedTimeOfArrival

Optional. Only provided if the vehicle has arrived at this stop. ISO 8601, UTC.

`observedTimeOfArrival`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-call-properties-observedtimeofarrival.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfArrival")

#### observedTimeOfArrival Type

`string`

### estimatedTimeOfDeparture

Optional. Usually not provided for the last call of the journey. ISO 8601, UTC.

`estimatedTimeOfDeparture`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofdeparture.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfDeparture")

#### estimatedTimeOfDeparture Type

`string`

### observedTimeOfDeparture

Optional. Only provided if the vehicle has departed from this stop. ISO 8601, UTC.

`observedTimeOfDeparture`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-call-properties-observedtimeofdeparture.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfDeparture")

#### observedTimeOfDeparture Type

`string`

### restriction

Optional. Only provided if boarding or alighting restriction applies based on a combination of planned restrictions and partial journey cancellations. Possible values in examples.

`restriction`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-call-properties-restriction.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/restriction")

#### restriction Type

`string`

#### restriction Examples

```json
"NO_BOARDING"
```

```json
"NO_ALIGHTING"
```

```json
"NO_STOP"
```

## Definitions group tariffZoneInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo"}
```

| Property          | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                           |
| :---------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)       | `string` | Required | cannot be null | [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-ref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/ref")       |
| [number](#number) | `string` | Required | cannot be null | [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-number.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/number") |
| [code](#code)     | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-code.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/code")     |
| [name](#name)     | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/name")     |

### ref

A unique identifier.

`ref`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-ref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/ref")

#### ref Type

`string`

### number

The number of the tariff zone unique within the transport authority.

`number`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-number.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/number")

#### number Type

`string`

### code

Optional. Short abbreviation.

`code`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-code.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/code")

#### code Type

`string`

### name

Optional. Full name.

`name`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [ExpectedCall](expected-call-definitions-tariff-zone-info-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/tariffZoneInfo/properties/name")

#### name Type

`string`
