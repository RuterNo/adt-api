# Journey Pattern Point Info Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## journeyPatternPointInfo Type

`object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-journey-pattern-point-info.md))

# journeyPatternPointInfo Properties

| Property                                      | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                       |
| :-------------------------------------------- | :-------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)                                   | `string`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-ref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/ref")                                   |
| [isTimingPoint](#istimingpoint)               | `boolean` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-istimingpoint.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/isTimingPoint")               |
| [location](#location)                         | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-position.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/location")                                                               |
| [distanceFromPrevious](#distancefromprevious) | `number`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-distancefromprevious.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/distanceFromPrevious") |
| [tariffZones](#tariffzones)                   | `array`   | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-tariffzones.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/tariffZones")                   |

## ref

Id of journey pattern point.

`ref`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-ref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/ref")

### ref Type

`string`

## isTimingPoint

Boolean that indicates if this is a point where the driver should respect the departure time.

`isTimingPoint`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-istimingpoint.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/isTimingPoint")

### isTimingPoint Type

`boolean`

### isTimingPoint Examples

```json
"true"
```

```json
"false"
```

## location

Optional. The position of the point in Latitude/Longitude.

`location`

*   is optional

*   Type: `object` ([Position](vehicle-journey-details-definitions-position.md))

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-position.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/location")

### location Type

`object` ([Position](vehicle-journey-details-definitions-position.md))

## distanceFromPrevious

Optional. Meters from previous point. The first call has the value zero.

`distanceFromPrevious`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-distancefromprevious.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/distanceFromPrevious")

### distanceFromPrevious Type

`number`

## tariffZones

Optional. Tariff Zones valid for this point.

`tariffZones`

*   is optional

*   Type: `object[]` ([Tariff Zone Info](vehicle-journey-details-definitions-tariff-zone-info.md))

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-tariffzones.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/tariffZones")

### tariffZones Type

`object[]` ([Tariff Zone Info](vehicle-journey-details-definitions-tariff-zone-info.md))
