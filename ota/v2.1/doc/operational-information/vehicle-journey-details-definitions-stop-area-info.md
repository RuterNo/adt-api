# Stop Area Info Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## stopAreaInfo Type

`object` ([Stop Area Info](vehicle-journey-details-definitions-stop-area-info.md))

# Stop Area Info Properties

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                               |
| :---------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)             | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/ref")             |
| [name](#name)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/name")           |
| [shortName](#shortname) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/shortName") |

## ref

Id of the Stop Area.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/ref")

### ref Type

`string`

## name

Full name. Max 50 characters.


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/name")

### name Type

`string`

## shortName

Optional. Shortened name. Max 16 characters.


`shortName`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/shortName")

### shortName Type

`string`
