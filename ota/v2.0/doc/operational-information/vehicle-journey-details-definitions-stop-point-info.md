# Stop Point Info Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## stopPointInfo Type

`object` ([Stop Point Info](vehicle-journey-details-definitions-stop-point-info.md))

# Stop Point Info Properties

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                         |
| :------------------------------ | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)                     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/ref")                     |
| [name](#name)                   | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/name")                   |
| [shortName](#shortname)         | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/shortName")         |
| [designation](#designation)     | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/designation")     |
| [localNumber](#localnumber)     | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-localnumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/localNumber")     |
| [length](#length)               | `number` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-length.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/length")               |
| [stopPointKeys](#stoppointkeys) | `array`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-stoppointkeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/stopPointKeys") |

## ref

Id of the Stop Area.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/ref")

### ref Type

`string`

## name

Full name. Max 50 characters.


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/name")

### name Type

`string`

## shortName

Optional. Shortened name. Max 16 characters.


`shortName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/shortName")

### shortName Type

`string`

## designation

Optional. Track, gate, stop etc. as shown to the public. This is for local orientation within a stop area, bus terminal or station.


`designation`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/designation")

### designation Type

`string`

## localNumber

The display order of stops within a stop area.


`localNumber`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-localnumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/localNumber")

### localNumber Type

`number`

## length

Optional. The stops capacity in meters.


`length`

-   is optional
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-length.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/length")

### length Type

`number`

## stopPointKeys

Optional. Array with point specific information.


`stopPointKeys`

-   is optional
-   Type: `object[]` ([Key](vehicle-journey-details-definitions-key.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-stoppointkeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/stopPointKeys")

### stopPointKeys Type

`object[]` ([Key](vehicle-journey-details-definitions-key.md))
