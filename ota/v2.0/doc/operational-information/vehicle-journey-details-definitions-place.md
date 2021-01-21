# Place Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## place Type

`object` ([Place](vehicle-journey-details-definitions-place.md))

# Place Properties

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                               |
| :---------------------- | -------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)           | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/name")           |
| [shortName](#shortname) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/shortName") |

## name

Optional. Name of the origin.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/name")

### name Type

`string`

## shortName

Optional. Short name of the origin.


`shortName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/shortName")

### shortName Type

`string`
