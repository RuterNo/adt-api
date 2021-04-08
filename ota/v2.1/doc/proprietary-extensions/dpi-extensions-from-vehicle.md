# [v2.1](../../README.md) / [Proprietary extensions](README.md) / Dpi extensions from vehicle 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/pe/dpi/#```  | ```false``` | ```0```

# DpiExtensionsFromVehicle Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/proprietary-extensions/dpi-extensions-from-vehicle.json
```

It is in Ruters interest to provide a rich and dynamic personal user experience onboard our vehicles. To provide flexibility these two topics and corresponding subtopics must be bridged between Ruter BO and the vehicle. Data will be produced and consumed only by Ruters systems.

No payload structure is defined.


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                      |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [dpi-extensions-from-vehicle.json](../../schema/proprietary-extensions/dpi-extensions-from-vehicle.json "open original schema") |

## DpiExtensionsFromVehicle Type

`object` ([DpiExtensionsFromVehicle](dpi-extensions-from-vehicle.md))

## DpiExtensionsFromVehicle Examples

```json
{
  "arbitrary-key": "arbitraryValue"
}
```

# DpiExtensionsFromVehicle Properties

| Property              | Type | Required | Nullable    | Defined by |
| :-------------------- | ---- | -------- | ----------- | :--------- |
| Additional Properties | Any  | Optional | can be null |            |

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
