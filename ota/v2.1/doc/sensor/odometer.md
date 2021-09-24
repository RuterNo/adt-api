# [v2.1](../../README.md) / [Sensor](README.md) / Odometer 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/sensors/odometer```  | ```false``` | ```0```

# Odometer Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/sensor/odometer.json
```

Describes an odometer value in meters based on total vehicle distance or similar. Absolute value of less importance but should be increasing at least within the scope of a journey. Optionally the current speed according to the odometer could be included.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [odometer.json](../../schema/sensor/odometer.json "open original schema") |

## Odometer Type

`object` ([Odometer](odometer.md))

## Odometer Examples

```json
{
  "distance": 23434556,
  "atDateTime": "2017-11-30T23:45:52.006Z",
  "messageNumber": 12345
}
```

# Odometer Properties

| Property                        | Type     | Required | Nullable       | Defined by                                                                                              |
| :------------------------------ | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------ |
| [distance](#distance)           | `number` | Required | cannot be null | [Odometer](odometer-properties-distance.md "#/properties/distance#/properties/distance")                |
| [atDateTime](#atdatetime)       | `string` | Required | cannot be null | [Odometer](odometer-properties-atdatetime.md "#/properties/atDateTime#/properties/atDateTime")          |
| [messageNumber](#messagenumber) | `number` | Optional | cannot be null | [Odometer](odometer-properties-messagenumber.md "#/properties/messageNumber#/properties/messageNumber") |
| Additional Properties           | Any      | Optional | can be null    |                                                                                                         |

## distance

Describes absolute odometer value in metres.

`distance`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [Odometer](odometer-properties-distance.md "#/properties/distance#/properties/distance")

### distance Type

`number`

## atDateTime

ISO 8601. Reflects the UTC time when the state changed.

`atDateTime`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Odometer](odometer-properties-atdatetime.md "#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## messageNumber

Optional. Sequence number, increased by one for each new message. Used to validate consistency in the data stream.

> Added in version 2.1

`messageNumber`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [Odometer](odometer-properties-messagenumber.md "#/properties/messageNumber#/properties/messageNumber")

### messageNumber Type

`number`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
