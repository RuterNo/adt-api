# Tariff Zone Info Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## tariffZoneInfo Type

`object` ([Tariff Zone Info](vehicle-journey-details-definitions-tariff-zone-info.md))

# Tariff Zone Info Properties

| Property          | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                             |
| :---------------- | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/ref")       |
| [number](#number) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/number") |
| [code](#code)     | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/code")     |
| [name](#name)     | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/name")     |

## ref

A unique identifier.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/ref")

### ref Type

`string`

## number

The number of the tariff zone unique within the transport authority.


`number`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/number")

### number Type

`string`

## code

Optional. Short abbreviation.


`code`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/code")

### code Type

`string`

## name

Optional. Full name.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/name")

### name Type

`string`
