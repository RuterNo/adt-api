# Connection Info Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## connectionInfo Type

`object` ([Connection Info](vehicle-journey-details-definitions-connection-info.md))

# connectionInfo Properties

| Property                                              | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                           |
| :---------------------------------------------------- | :------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [connectionRef](#connectionref)                       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-connectionref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/connectionRef")                       |
| [transportModeCode](#transportmodecode)               | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-transportmodecode.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/transportModeCode")               |
| [lineAuthorityCode](#lineauthoritycode)               | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-lineauthoritycode.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineAuthorityCode")               |
| [lineDesignation](#linedesignation)                   | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-linedesignation.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineDesignation")                   |
| [directionName](#directionname)                       | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-directionname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/directionName")                       |
| [stopAreaName](#stopareaname)                         | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stopareaname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopAreaName")                         |
| [stopPointDesignation](#stoppointdesignation)         | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stoppointdesignation.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopPointDesignation")         |
| [minChangeDurationSeconds](#minchangedurationseconds) | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-minchangedurationseconds.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/minChangeDurationSeconds") |
| [maxWaitingUntilTime](#maxwaitinguntiltime)           | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-maxwaitinguntiltime.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/maxWaitingUntilTime")           |

## connectionRef

Identifier used for matching with real-time data in later stage. Is unique in scope of current vehicle journey and call sequenceNumber. Typically has the value of the connecting journeys directionOfLineRef.

`connectionRef`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-connectionref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/connectionRef")

### connectionRef Type

`string`

## transportModeCode

The transport mode. Possible values in examples.

`transportModeCode`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-transportmodecode.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/transportModeCode")

### transportModeCode Type

`string`

### transportModeCode Examples

```json
"BUS"
```

```json
"TRAM"
```

## lineAuthorityCode

Short abbreviation for the organisation providing the connecting journey. Possible values in examples.

`lineAuthorityCode`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-lineauthoritycode.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineAuthorityCode")

### lineAuthorityCode Type

`string`

### lineAuthorityCode Examples

```json
"SJ"
```

```json
"ÖTåg"
```

```json
"SL"
```

## lineDesignation

The public line number displayed to passengers for the connecting journey. Observe that this value can be alphanumeric!

`lineDesignation`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-linedesignation.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineDesignation")

### lineDesignation Type

`string`

## directionName

Optional. Name of direction for connecting journey.

`directionName`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-directionname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/directionName")

### directionName Type

`string`

## stopAreaName

Optional. Name of stop for the connecting journey. Only included if different stop than the stop this vehicle stops at.

`stopAreaName`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stopareaname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopAreaName")

### stopAreaName Type

`string`

## stopPointDesignation

Optional. Platform/track/gate number or letter as shown to the public for the stop of the connecting journey. This is for local orientation within a stop area, bus terminal or station.

`stopPointDesignation`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stoppointdesignation.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopPointDesignation")

### stopPointDesignation Type

`string`

## minChangeDurationSeconds

The minimum number of seconds needed to transfer (walk) between the involved vehicles. May need to be multiplied by some factors depending on different passenger abilities.

`minChangeDurationSeconds`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-minchangedurationseconds.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/minChangeDurationSeconds")

### minChangeDurationSeconds Type

`number`

## maxWaitingUntilTime

Optional. The date and time when the connection guarantee ends. The fetcher vehicle may leave at this time even if feeder vehicle has not yet arrived. ISO 8601, UTC.

`maxWaitingUntilTime`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-maxwaitinguntiltime.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/maxWaitingUntilTime")

### maxWaitingUntilTime Type

`string`
