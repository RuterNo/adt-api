# Untitled array in VehicleJourneyDetails Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/fetcherConnections
```

Optional. Planned fetcher (distributor) protected connections. A list of vehicle journeys that must wait for passengers from this vehicle journey at this stop even if it is delayed. Relevant for passenger information.


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## fetcherConnections Type

`object[]` ([Connection Info](vehicle-journey-details-definitions-connection-info.md))
