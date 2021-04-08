# Untitled boolean in VehicleJourneyDetails Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/isCancelledCall
```

Optional. Only provided if true. Boolean that indicates if this is call is cancelled without being replaced. In this case the call to the above-mentioned stop should be presented as cancelled.


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## isCancelledCall Type

`boolean`

## isCancelledCall Examples

```json
"true"
```

```json
"false"
```
