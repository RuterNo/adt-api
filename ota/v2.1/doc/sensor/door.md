# [v2.1](../../README.md) / [Sensor](README.md) / Door 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/sensors/door```  | ```true``` | ```1```

# Door Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/sensor/door.json
```

Describes if any door is open (or to be more precise – if the door lock is released). Also see topic pe/doors_individually for status on individual doors.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                        |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ----------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [door.json](../../schema/sensor/door.json "open original schema") |

## Door Type

`object` ([Door](door.md))

## Door Examples

```json
{
  "doorOpen": true,
  "atDateTime": "2021-11-30T23:45:52.006Z"
}
```

# Door Properties

| Property                  | Type      | Required | Nullable       | Defined by                                                                              |
| :------------------------ | --------- | -------- | -------------- | :-------------------------------------------------------------------------------------- |
| [doorOpen](#dooropen)     | `boolean` | Required | cannot be null | [Door](door-properties-dooropen.md "\#/properties/doorOpen#/properties/doorOpen")       |
| [atDateTime](#atdatetime) | `string`  | Required | cannot be null | [Door](door-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime") |
| Additional Properties     | Any       | Optional | can be null    |                                                                                         |

## doorOpen

True if any door is open (door lock is released). False if door lock is activated.


`doorOpen`

-   is required
-   Type: `boolean`
-   cannot be null
-   defined in: [Door](door-properties-dooropen.md "\#/properties/doorOpen#/properties/doorOpen")

### doorOpen Type

`boolean`

### doorOpen Examples

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
-   defined in: [Door](door-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
