# Point Call Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## pointCall Type

`object` ([Point Call](vehicle-journey-details-definitions-point-call.md))

# Point Call Properties

| Property                                                    | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                                                          |
| :---------------------------------------------------------- | --------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [sequenceNumber](#sequencenumber)                           | `number`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-sequencenumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/sequenceNumber")         |
| [journeyPatternPoint](#journeypatternpoint)                 | `object`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/journeyPatternPoint")              |
| [stopArea](#stoparea)                                       | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopArea")                                     |
| [stopPoint](#stoppoint)                                     | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopPoint")                                   |
| [arrival](#arrival)                                         | `object`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/arrival")                                             |
| [departure](#departure)                                     | `object`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-departure.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/departure")                                         |
| [destinationDisplay](#destinationdisplay)                   | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/destinationDisplay")                      |
| [isCancelledCall](#iscancelledcall)                         | `boolean` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-iscancelledcall.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/isCancelledCall")       |
| [replacedJourneyPatternPoint](#replacedjourneypatternpoint) | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedJourneyPatternPoint")      |
| [replacedStopArea](#replacedstoparea)                       | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopArea")                             |
| [replacedStopPoint](#replacedstoppoint)                     | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopPoint")                           |
| [fetcherConnections](#fetcherconnections)                   | `array`   | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-fetcherconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/fetcherConnections") |
| [feederConnections](#feederconnections)                     | `array`   | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-feederconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/feederConnections")   |

## sequenceNumber

The order of the call on the vehicle journey. Increasing. Note that the numbering can start with a higher number than 1 and that there might be holes in the sequence numbering as not expected calls are excluded.


`sequenceNumber`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-sequencenumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/sequenceNumber")

### sequenceNumber Type

`number`

## journeyPatternPoint

The point to call. (May be updated in real time).


`journeyPatternPoint`

-   is required
-   Type: `object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-journey-pattern-point-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/journeyPatternPoint")

### journeyPatternPoint Type

`object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-journey-pattern-point-info.md))

## stopArea

Optional. The stop area of the call. (May be updated in real time).


`stopArea`

-   is optional
-   Type: `object` ([Stop Area Info](vehicle-journey-details-definitions-stop-area-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopArea")

### stopArea Type

`object` ([Stop Area Info](vehicle-journey-details-definitions-stop-area-info.md))

## stopPoint

Optional. The stop point of the call. (May be updated in real time).


`stopPoint`

-   is optional
-   Type: `object` ([Stop Point Info](vehicle-journey-details-definitions-stop-point-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopPoint")

### stopPoint Type

`object` ([Stop Point Info](vehicle-journey-details-definitions-stop-point-info.md))

## arrival




`arrival`

-   is required
-   Type: `object` ([Arrival](vehicle-journey-details-definitions-arrival.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/arrival")

### arrival Type

`object` ([Arrival](vehicle-journey-details-definitions-arrival.md))

## departure




`departure`

-   is required
-   Type: `object` ([Departure](vehicle-journey-details-definitions-departure.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-departure.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/departure")

### departure Type

`object` ([Departure](vehicle-journey-details-definitions-departure.md))

## destinationDisplay

Optional.


`destinationDisplay`

-   is optional
-   Type: `object` ([Destination Display](vehicle-journey-details-definitions-destination-display.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/destinationDisplay")

### destinationDisplay Type

`object` ([Destination Display](vehicle-journey-details-definitions-destination-display.md))

## isCancelledCall

Optional. Only provided if true. Boolean that indicates if this is call is cancelled without being replaced. In this case the call to the above-mentioned stop should be presented as cancelled.


`isCancelledCall`

-   is optional
-   Type: `boolean`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-iscancelledcall.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/isCancelledCall")

### isCancelledCall Type

`boolean`

### isCancelledCall Examples

```json
"true"
```

```json
"false"
```

## replacedJourneyPatternPoint

Optional. Only provided if the original Journey Pattern Point is replaced. Describes the replaced point. Represents the original (planned) information.


`replacedJourneyPatternPoint`

-   is optional
-   Type: `object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-journey-pattern-point-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedJourneyPatternPoint")

### replacedJourneyPatternPoint Type

`object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-journey-pattern-point-info.md))

## replacedStopArea

Optional. Only present if the original StopArea is replaced. Describes the replaced stop area. Represents the original (planned) information.


`replacedStopArea`

-   is optional
-   Type: `object` ([Stop Area Info](vehicle-journey-details-definitions-stop-area-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopArea")

### replacedStopArea Type

`object` ([Stop Area Info](vehicle-journey-details-definitions-stop-area-info.md))

## replacedStopPoint

Optional. Only present if the original StopPoint is replaced. Describes the replaced stop point. Represents the original (planned) information.


`replacedStopPoint`

-   is optional
-   Type: `object` ([Stop Point Info](vehicle-journey-details-definitions-stop-point-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopPoint")

### replacedStopPoint Type

`object` ([Stop Point Info](vehicle-journey-details-definitions-stop-point-info.md))

## fetcherConnections

Optional. Planned fetcher (distributor) protected connections. A list of vehicle journeys that must wait for passengers from this vehicle journey at this stop even if it is delayed. Relevant for passenger information.


`fetcherConnections`

-   is optional
-   Type: `object[]` ([Connection Info](vehicle-journey-details-definitions-connection-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-fetcherconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/fetcherConnections")

### fetcherConnections Type

`object[]` ([Connection Info](vehicle-journey-details-definitions-connection-info.md))

## feederConnections

Optional. Planned feeder protected connections. A list of vehicle journeys that this vehicle journey should await passengers from at this stop even if the feeding journeys are delayed. Relevant for driver information.


`feederConnections`

-   is optional
-   Type: `object[]` ([Connection Info](vehicle-journey-details-definitions-connection-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-feederconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/feederConnections")

### feederConnections Type

`object[]` ([Connection Info](vehicle-journey-details-definitions-connection-info.md))
