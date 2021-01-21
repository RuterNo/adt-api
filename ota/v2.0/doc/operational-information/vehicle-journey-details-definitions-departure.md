# Departure Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## departure Type

`object` ([Departure](vehicle-journey-details-definitions-departure.md))

# Departure Properties

| Property                              | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                     |
| :------------------------------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [earliestDateTime](#earliestdatetime) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-earliestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/earliestDateTime") |
| [departureType](#departuretype)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-departuretype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/departureType")       |

## earliestDateTime

The earliest permitted departure time according to original plan. Departure before this time is EARLY. ISO 8601, UTC.


`earliestDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-earliestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/earliestDateTime")

### earliestDateTime Type

`string`

## departureType

Usage of the departure according to original plan. NoStop and StopNoAlighting means that the arrival should NOT be presented public.


`departureType`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-departuretype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/departureType")

### departureType Type

`string`
