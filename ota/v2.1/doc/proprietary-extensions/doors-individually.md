# [v2.1](../../README.md) / [Proprietary extensions](README.md) / Doors individually 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/pe/doors_individually```  | ```false``` | ```1```

# DoorsIndividually Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/proprietary-extensions/doors-individually.json
```

This topic is used to track the individual status of doors. One use case is to improve the data quality of APC counts. See also topic sensors/door for status of anyDoorOpen/allDoorsClosed.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                    |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [doors-individually.json](../../schema/proprietary-extensions/doors-individually.json "open original schema") |

## DoorsIndividually Type

`object` ([DoorsIndividually](doors-individually.md))

## DoorsIndividually Examples

```json
{
  "doorRef": "01",
  "isOpen": true,
  "atDateTime": "2021-10-31T12:45:50Z"
}
```

# DoorsIndividually Properties

| Property                  | Type      | Required | Nullable       | Defined by                                                                                                        |
| :------------------------ | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------- |
| [doorRef](#doorref)       | `string`  | Required | cannot be null | [DoorsIndividually](doors-individually-properties-doorref.md "#/properties/doorRef#/properties/doorRef")          |
| [isOpen](#isopen)         | `boolean` | Required | cannot be null | [DoorsIndividually](doors-individually-properties-isopen.md "#/properties/isOpen#/properties/isOpen")             |
| [atDateTime](#atdatetime) | `string`  | Required | cannot be null | [DoorsIndividually](doors-individually-properties-atdatetime.md "#/properties/atDateTime#/properties/atDateTime") |
| Additional Properties     | Any       | Optional | can be null    |                                                                                                                   |

## doorRef

Has to be the same reference as is used in the topic sensors/apc_sensors.

`doorRef`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DoorsIndividually](doors-individually-properties-doorref.md "#/properties/doorRef#/properties/doorRef")

### doorRef Type

`string`

## isOpen

True if the door is open.

`isOpen`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [DoorsIndividually](doors-individually-properties-isopen.md "#/properties/isOpen#/properties/isOpen")

### isOpen Type

`boolean`

### isOpen Examples

```json
"true"
```

```json
"false"
```

## atDateTime

Timestamp when isOpen has changed, ISO 8601

`atDateTime`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DoorsIndividually](doors-individually-properties-atdatetime.md "#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
