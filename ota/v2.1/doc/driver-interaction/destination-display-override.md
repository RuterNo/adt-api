# [v2.1](../../README.md) / [Driver interaction](README.md) / Destination display override 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/di/override_attempt/destination_display```  | ```false``` | ```0```

# DestinationDisplayOverride Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/driver-interaction/destination-display-override.json
```

Describes a request from MADT or other GUI to manually override the information shown on the destination display. It is up to the presenting system to decide how and for how long the override will apply. A rule could be until next journey begins or a new override_attempt/destination_display is received. The topic could be blanked (provided with a zero-byte payload) to indicate that any overriding information is no longer valid and that the destination display can return to normal


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                    |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [destination-display-override.json](../../schema/driver-interaction/destination-display-override.json "open original schema") |

## DestinationDisplayOverride Type

`object` ([DestinationDisplayOverride](destination-display-override.md))

## DestinationDisplayOverride Examples

```json
{
  "number": 666
}
```

# DestinationDisplayOverride Properties

| Property              | Type     | Required | Nullable       | Defined by                                                                                                                |
| :-------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------ |
| [number](#number)     | `number` | Required | cannot be null | [DestinationDisplayOverride](destination-display-override-properties-number.md "\#/properties/number#/properties/number") |
| Additional Properties | Any      | Optional | can be null    |                                                                                                                           |

## number

Numeric value representing the destination sign information to display.


`number`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [DestinationDisplayOverride](destination-display-override-properties-number.md "\#/properties/number#/properties/number")

### number Type

`number`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
