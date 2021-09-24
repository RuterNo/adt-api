# Position Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/position
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## position Type

`object` ([Position](vehicle-journey-details-definitions-position.md))

# position Properties

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                |
| :---------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [latitude](#latitude)   | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-latitude.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/position/properties/latitude")   |
| [longitude](#longitude) | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-longitude.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/position/properties/longitude") |

## latitude

The latitude in decimal degrees.

`latitude`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-latitude.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/position/properties/latitude")

### latitude Type

`number`

## longitude

The longitude in decimal degrees.

`longitude`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-longitude.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/position/properties/longitude")

### longitude Type

`number`
