# Organisation Info Schema

```txt
#/properties/transportAuthority#/properties/transportAuthority
```

Information about the transport authority that provides the journey.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## transportAuthority Type

`object` ([Organisation Info](vehicle-journey-details-properties-organisation-info.md))

# transportAuthority Properties

| Property          | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                           |
| :---------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-ref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/ref")       |
| [code](#code)     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-code.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/code")     |
| [name](#name)     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/name")     |
| [number](#number) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-number.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/number") |

## ref

A unique identifier.

`ref`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-ref.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/ref")

### ref Type

`string`

## code

Short abbreviation.

`code`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-code.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/code")

### code Type

`string`

## name

Full name.

`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-name.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/name")

### name Type

`string`

## number

The number of the object that the organisation info refers to. Transport Authority number or Contractor Number.

`number`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-number.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/number")

### number Type

`string`
