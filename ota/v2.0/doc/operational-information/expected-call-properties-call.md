# Call Schema

```txt
#/properties/previousCall#/properties/previousCall
```

Optional. Describes the call to the stop immediately preceding the expected call. Only provided if there is at least one call in the journey before the expected call.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                             |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [expected-call.json\*](../../schema/operational-information/expected-call.json "open original schema") |

## previousCall Type

`object` ([Call](expected-call-properties-call.md))

# Call Properties

| Property                                              | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                              |
| :---------------------------------------------------- | -------- | -------- | -------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [callSequenceNumber](#callsequencenumber)             | `number` | Required | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-callsequencenumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/callSequenceNumber")             |
| [pointRef](#pointref)                                 | `string` | Required | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-pointref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/pointRef")                                 |
| [estimatedTimeOfArrival](#estimatedtimeofarrival)     | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofarrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfArrival")     |
| [observedTimeOfArrival](#observedtimeofarrival)       | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-observedtimeofarrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfArrival")       |
| [estimatedTimeOfDeparture](#estimatedtimeofdeparture) | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofdeparture.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfDeparture") |
| [observedTimeOfDeparture](#observedtimeofdeparture)   | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-observedtimeofdeparture.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfDeparture")   |
| [restriction](#restriction)                           | `string` | Optional | cannot be null | [ExpectedCall](expected-call-definitions-call-properties-restriction.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/restriction")                           |

## callSequenceNumber

Order number of stop in journey pattern. (One-based list).


`callSequenceNumber`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [ExpectedCall](expected-call-definitions-call-properties-callsequencenumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/callSequenceNumber")

### callSequenceNumber Type

`number`

## pointRef

A stop identifier.


`pointRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [ExpectedCall](expected-call-definitions-call-properties-pointref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/pointRef")

### pointRef Type

`string`

## estimatedTimeOfArrival

Optional. Only provided if the vehicle has not arrived at this stop. ISO 8601, UTC.


`estimatedTimeOfArrival`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofarrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfArrival")

### estimatedTimeOfArrival Type

`string`

## observedTimeOfArrival

Optional. Only provided if the vehicle has arrived at this stop. ISO 8601, UTC.


`observedTimeOfArrival`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [ExpectedCall](expected-call-definitions-call-properties-observedtimeofarrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfArrival")

### observedTimeOfArrival Type

`string`

## estimatedTimeOfDeparture

Optional. Usually not provided for the last call of the journey. ISO 8601, UTC.


`estimatedTimeOfDeparture`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [ExpectedCall](expected-call-definitions-call-properties-estimatedtimeofdeparture.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/estimatedTimeOfDeparture")

### estimatedTimeOfDeparture Type

`string`

## observedTimeOfDeparture

Optional. Only provided if the vehicle has departed from this stop. ISO 8601, UTC.


`observedTimeOfDeparture`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [ExpectedCall](expected-call-definitions-call-properties-observedtimeofdeparture.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/observedTimeOfDeparture")

### observedTimeOfDeparture Type

`string`

## restriction

Optional. Only provided if boarding or alighting restriction applies based on a combination of planned restrictions and partial journey cancellations. Possible values in examples.


`restriction`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [ExpectedCall](expected-call-definitions-call-properties-restriction.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/expected-call.json#/definitions/call/properties/restriction")

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
