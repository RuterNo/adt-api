# Secondary Destination Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## secondaryDestination Type

`object` ([Secondary Destination](vehicle-journey-details-definitions-secondary-destination.md))

# secondaryDestination Properties

| Property                                              | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                       |
| :---------------------------------------------------- | :------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                                         | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/name")                                         |
| [shortName](#shortname)                               | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-shortname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/shortName")                               |
| [secondaryDestinationType](#secondarydestinationtype) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-secondarydestinationtype.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/secondaryDestinationType") |

## name

Optional. Name of the destination.

`name`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/name")

### name Type

`string`

## shortName

Optional. Short name of the destination.

`shortName`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-shortname.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/shortName")

### shortName Type

`string`

## secondaryDestinationType

Optional. The meaning of the secondary destination.

`secondaryDestinationType`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-secondarydestinationtype.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/secondaryDestinationType")

### secondaryDestinationType Type

`string`
