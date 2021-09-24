# Primary Destination Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/primaryDestination
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## primaryDestination Type

`object` ([Primary Destination](vehicle-journey-details-definitions-primary-destination.md))

# primaryDestination Properties

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                     |
| :---------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/name")           |
| [shortName](#shortname) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-shortname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/shortName") |

## name

Name of the destination.

`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/name")

### name Type

`string`

## shortName

Optional. Short name of the destination.

`shortName`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-shortname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/shortName")

### shortName Type

`string`
