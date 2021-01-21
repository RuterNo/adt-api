# [v2.0](../../README.md) / [Sensor](README.md) / Apc sensors 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/sensors/apc_sensors```  | ```true``` | ```1```

# ApcSensors Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/sensor/apc-sensors.json
```

Raw-data from door-sensor for later evaluation.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                      |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [apc-sensors.json](../../schema/sensor/apc-sensors.json "open original schema") |

## ApcSensors Type

`object` ([ApcSensors](apc-sensors.md))

## ApcSensors Examples

```json
{
  "doorRef": "01",
  "alightingCount": 23,
  "boardingCount": 12,
  "atDateTime": "2017-10-31T12:45:50Z",
  "categoryActivities": [
    {
      "categoryRef": "ADULT",
      "alightingCount": 23,
      "boardingCount": 9
    },
    {
      "categoryRef": "CHILD",
      "alightingCount": 0,
      "boardingCount": 3
    }
  ]
}
```

# ApcSensors Properties

| Property                                  | Type     | Required | Nullable       | Defined by                                                                                                                   |
| :---------------------------------------- | -------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| [doorRef](#doorref)                       | `string` | Required | cannot be null | [ApcSensors](apc-sensors-properties-doorref.md "\#/properties/doorRef#/properties/doorRef")                                  |
| [alightingCount](#alightingcount)         | `number` | Required | cannot be null | [ApcSensors](apc-sensors-properties-alightingcount.md "\#/properties/alightingCount#/properties/alightingCount")             |
| [boardingCount](#boardingcount)           | `number` | Required | cannot be null | [ApcSensors](apc-sensors-properties-boardingcount.md "\#/properties/alightingCount#/properties/boardingCount")               |
| [atDateTime](#atdatetime)                 | `string` | Required | cannot be null | [ApcSensors](apc-sensors-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")                         |
| [categoryActivities](#categoryactivities) | `array`  | Required | cannot be null | [ApcSensors](apc-sensors-properties-categoryactivities.md "\#/properties/categoryActivities#/properties/categoryActivities") |
| Additional Properties                     | Any      | Optional | can be null    |                                                                                                                              |

## doorRef

Stable alfa-numeric reference that is unique within scope of vehicle (vehicle element/train set). Could be a door-number or a combination of coach number and door number.


`doorRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [ApcSensors](apc-sensors-properties-doorref.md "\#/properties/doorRef#/properties/doorRef")

### doorRef Type

`string`

## alightingCount

Accumulated number of alighting passengers detected by this sensor since last reset.


`alightingCount`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [ApcSensors](apc-sensors-properties-alightingcount.md "\#/properties/alightingCount#/properties/alightingCount")

### alightingCount Type

`number`

## boardingCount

Accumulated number of boarding passengers detected by this sensor since last reset.


`boardingCount`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [ApcSensors](apc-sensors-properties-boardingcount.md "\#/properties/alightingCount#/properties/boardingCount")

### boardingCount Type

`number`

## atDateTime

ISO 8601. Reflects the current UTC time.


`atDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [ApcSensors](apc-sensors-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## categoryActivities

A list describing APC activity at each individual door divided per handled object category.


`categoryActivities`

-   is required
-   Type: `object[]` ([Details](apc-sensors-properties-categoryactivities-items.md))
-   cannot be null
-   defined in: [ApcSensors](apc-sensors-properties-categoryactivities.md "\#/properties/categoryActivities#/properties/categoryActivities")

### categoryActivities Type

`object[]` ([Details](apc-sensors-properties-categoryactivities-items.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
