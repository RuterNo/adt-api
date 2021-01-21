# [v2.0](../../README.md) / [Sensor](README.md) / Stop button 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/sensors/stop_button```  | ```true``` | ```1```

# StopButton Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/sensor/stop-button.json
```

Describes if passengers have requested that the bus should stop (stop button pressed).


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                      |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [stop-button.json](../../schema/sensor/stop-button.json "open original schema") |

## StopButton Type

`object` ([StopButton](stop-button.md))

## StopButton Examples

```json
{
  "stopPressed": true,
  "atDateTime": "2021-11-30T23:45:52.006Z"
}
```

# StopButton Properties

| Property                    | Type      | Required | Nullable       | Defined by                                                                                              |
| :-------------------------- | --------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------ |
| [stopPressed](#stoppressed) | `boolean` | Required | cannot be null | [StopButton](stop-button-properties-stoppressed.md "\#/properties/stopPressed#/properties/stopPressed") |
| [atDateTime](#atdatetime)   | `string`  | Required | cannot be null | [StopButton](stop-button-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")    |
| Additional Properties       | Any       | Optional | can be null    |                                                                                                         |

## stopPressed

True if stop request button pressed. False if stop request signal is cleared.


`stopPressed`

-   is required
-   Type: `boolean`
-   cannot be null
-   defined in: [StopButton](stop-button-properties-stoppressed.md "\#/properties/stopPressed#/properties/stopPressed")

### stopPressed Type

`boolean`

### stopPressed Examples

```json
"true"
```

```json
"false"
```

## atDateTime

ISO 8601. Reflects the UTC time when the state changed.


`atDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [StopButton](stop-button-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
