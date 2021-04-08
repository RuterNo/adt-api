# Direction Of Line Info Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## directionOfLineInfo Type

`object` ([Direction Of Line Info](vehicle-journey-details-definitions-direction-of-line-info.md))

# Direction Of Line Info Properties

| Property      | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                    |
| :------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [code](#code) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/code") |
| [name](#name) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/name") |

## code

A value that is unique per direction.


`code`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/code")

### code Type

`string`

### code Examples

```json
"1"
```

```json
"2"
```

## name

Optional. Name of direction.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/name")

### name Type

`string`
