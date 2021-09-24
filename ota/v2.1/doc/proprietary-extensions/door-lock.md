# [v2.1](../../README.md) / [Proprietary extensions](README.md) / Door lock 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/pe/doorlock```  | ```false``` | ```1```

# DoorLock Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/proprietary-extensions/door-lock.json
```

This message is used to track if the tram doors are locked or unlocked.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [door-lock.json](../../schema/proprietary-extensions/door-lock.json "open original schema") |

## DoorLock Type

`object` ([DoorLock](door-lock.md))

## DoorLock Examples

```json
{
  "eventTimestamp": "2020-10-31T08:38:02.749Z",
  "locked": false
}
```

# DoorLock Properties

| Property                          | Type      | Required | Nullable       | Defined by                                                                                                  |
| :-------------------------------- | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------- |
| [eventTimestamp](#eventtimestamp) | `string`  | Required | cannot be null | [DoorLock](door-lock-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp") |
| [locked](#locked)                 | `boolean` | Required | cannot be null | [DoorLock](door-lock-properties-locked.md "#/properties/locked#/properties/locked")                         |
| Additional Properties             | Any       | Optional | can be null    |                                                                                                             |

## eventTimestamp

ISO 8601, UTC

`eventTimestamp`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DoorLock](door-lock-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp")

### eventTimestamp Type

`string`

## locked



`locked`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [DoorLock](door-lock-properties-locked.md "#/properties/locked#/properties/locked")

### locked Type

`boolean`

### locked Examples

```json
"true"
```

```json
"false"
```

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
