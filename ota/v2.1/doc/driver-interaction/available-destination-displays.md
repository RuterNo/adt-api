# [v2.1](../../README.md) / [Driver interaction](README.md) / Available destination displays 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/di/available_destination_displays```  | ```true``` | ```1```

# AvailableDestinationDisplays Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/driver-interaction/available-destination-displays.json
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                        |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [available-destination-displays.json](../../schema/driver-interaction/available-destination-displays.json "open original schema") |

## AvailableDestinationDisplays Type

`object` ([AvailableDestinationDisplays](available-destination-displays.md))

## AvailableDestinationDisplays Examples

```json
{
  "availableDestinationDisplays": [
    {
      "number": 12,
      "name": "Airport"
    },
    {
      "number": 112,
      "name": "Bus full"
    }
  ]
}
```

# AvailableDestinationDisplays Properties

| Property                                                      | Type    | Required | Nullable       | Defined by                                                                                                                                                                                      |
| :------------------------------------------------------------ | ------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [availableDestinationDisplays](#availabledestinationdisplays) | `array` | Required | cannot be null | [AvailableDestinationDisplays](available-destination-displays-properties-availabledestinationdisplays.md "\#/properties/availableDestinationDisplays#/properties/availableDestinationDisplays") |
| Additional Properties                                         | Any     | Optional | can be null    |                                                                                                                                                                                                 |

## availableDestinationDisplays




`availableDestinationDisplays`

-   is required
-   Type: `object[]` ([Details](available-destination-displays-properties-availabledestinationdisplays-items.md))
-   cannot be null
-   defined in: [AvailableDestinationDisplays](available-destination-displays-properties-availabledestinationdisplays.md "\#/properties/availableDestinationDisplays#/properties/availableDestinationDisplays")

### availableDestinationDisplays Type

`object[]` ([Details](available-destination-displays-properties-availabledestinationdisplays-items.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
