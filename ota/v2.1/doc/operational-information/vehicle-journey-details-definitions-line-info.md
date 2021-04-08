# Line Info Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## lineInfo Type

`object` ([Line Info](vehicle-journey-details-definitions-line-info.md))

# Line Info Properties

| Property                    | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                          |
| :-------------------------- | -------- | -------- | -------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)                 | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/ref")                 |
| [designation](#designation) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/designation") |
| [number](#number)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/number")           |
| [name](#name)               | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/name")               |

## ref

Optional. Only provided for service journeys. Information about the journey’s line.


`ref`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/ref")

### ref Type

`string`

## designation

The public line number displayed to passengers. Note: this value can be alphanumeric!


`designation`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/designation")

### designation Type

`string`

## number

Technical line number.


`number`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/number")

### number Type

`string`

## name

Optional. Name of line.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/name")

### name Type

`string`
