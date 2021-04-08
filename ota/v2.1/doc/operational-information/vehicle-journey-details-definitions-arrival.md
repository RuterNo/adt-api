# Arrival Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/arrival
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## arrival Type

`object` ([Arrival](vehicle-journey-details-definitions-arrival.md))

# Arrival Properties

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                             |
| :-------------------------------- | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [latestDateTime](#latestdatetime) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-latestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/latestDateTime") |
| [arrivalType](#arrivaltype)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-arrivaltype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/arrivalType")       |

## latestDateTime

The latest arrival time expected according to original plan. Arrival after this time is LATE. ISO 8601, UTC.


`latestDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-latestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/latestDateTime")

### latestDateTime Type

`string`

## arrivalType

Usage of the arrival according to original plan. NoStop and StopNoBoarding means that the departure should NOT be presented public.


`arrivalType`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-arrivaltype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/arrivalType")

### arrivalType Type

`string`
