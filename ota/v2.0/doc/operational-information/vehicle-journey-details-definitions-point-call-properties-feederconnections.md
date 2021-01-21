# Untitled array in VehicleJourneyDetails Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/FeederConnections
```

Optional. Planned feeder protected connections. A list of vehicle journeys that this vehicle journey should await passengers from at this stop even if the feeding journeys are delayed. Relevant for driver information.


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## FeederConnections Type

`object[]` ([Connection Info](vehicle-journey-details-definitions-connection-info.md))
