# Untitled array in VehicleJourneyDetails Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/displayKeys
```

Optional. Contains device specific information such as sign codes etcetera. See 5.6.20. A numeric sign code representing the combined destination display information could thus be provided in a contained key with appropriate parameterData. E.g. “Destination=659” It is possible to provide information for multiple display devices in parallel if there is a mixed fleet with different hardware by providing multiple Keys in parallel. E.g. one Key with "deviceName": "SIGN_X" and another Key with "deviceName": "SIGN_Y".


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## displayKeys Type

`object[]` ([Key](vehicle-journey-details-definitions-key.md))
