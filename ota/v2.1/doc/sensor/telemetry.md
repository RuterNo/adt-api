# [v2.1](../../README.md) / [Sensor](README.md) / Telemetry 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/sensors/telemetry/{sensorID}```  | ```false``` | ```0```

Several different kinds of sensor/telemetry data are available varying by vehicle type For traditional busses, FMS is the standard that defines what data about the vehicle is published on the FMS bus and further on by ITxPT FMStoIP [service.In](http://service.In "http://service.In") addition, vessels, trams and different bus types have proprietary data not captured by FMS.

According to the data centric approach from ITxPT, several of these data types (door, location, stop button etc) have been assigned separate topics as being described in this document. However, data types required by Ruter that haven’t yet been described in the MQTT structure from ITxPT, will still be handled by the general Telemetry topic that was introduced by Ruter in 2019.

All such data are defined by unique, 32 bit, identifiers. Data caught from the FMS bus retain their PGN numbers as the last 16 bits of the ID. Data not coming from the FMS bus follow a separate addressing scheme, with addresses allocated by Ruter on request. Please note that PTOs are free to decide if they want to use FMS or a non-FMS data source to provide the data.

To utilize FMS data in Ruter’s architecture, Operators can either set up an FMS2IP service or use any other means to subscribe to the FMS bus data. Note that there must be one separate MQTT message per FMS PGN.

The identifiers are constructed this way:


|Bytes | Description |
| --- | --- |
**1** | Source identifier (0x00 FMS, 0x01 Non-FMS)
**2-4** | Source-specific id, e.g. FMS PGNs

## Available Non-FMS standard data identifiers
Optional unless stated explicitly in the main ADT document.

ID | Subid | Name | Value | Recommended refresh interval | Remarks
--- | --- | --- | --- | --- | ---
**0001FF25** | 10003 | Wall Charger connected | | onChange |
**0001FF25** | 10004 | Fast Charger connected | | onChange |
**0001FF25** | 10005 | Charging Active | | onChange |
**01000002** | | Temperature inside average | float | 1/min |
**01000005** | | SOC | float | 1/min |
**01000006** | | Transmission mode | combustion/electric | onChange | Intended for hybrid vehicles
**01000007** | | Windscreen wiper active | True/false | onChange | Taken to represent a measurement of the ground truth binary rainfall state, given that it is a better predictor of the binary rainfall state than radar- or gauge-based measurements
**01000008** | | Accelerometry | | 1/min | * Bandwidth >= 100 hz<br> * Resolution <= 0.01 g
| | xmin | Min x value last minute | g | | |
| | xmax | Max x value last minute | g | | |
| | xavg | Average x value last minute | g | | |
| | ymin | Min y value last minute | g | | |
| | ymax | Max y value last minute | g | | |
| | yavg | Average y value last minute | g | | |
| | zmin | Min z value last minute | g | | |
| | zmax | Max z value last minute | g | | |
| | zavg | Average z value last minute | g | | |
**01000009** | | Outdoor temperature | float | 1/min |* Unit Celcius <br>* Resolution <= 1 C <br>* Measured at front of vehicle as near as possible to the ground
**0100000A** | | Accumulated energy consumption | float | 1/min | * Energy consumed <br>* Including HVAC <br>* Unit: kWh

# Telemetry Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/sensor/telemetry.json
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [telemetry.json](../../schema/sensor/telemetry.json "open original schema") |

## Telemetry Type

`object` ([Telemetry](telemetry.md))

## Telemetry Examples

```json
{
  "eventTimestamp": "2019-10-31T12:45:50Z",
  "id": "01000008",
  "payloads": [
    {
      "name": "xmin",
      "value": 0.1
    },
    {
      "name": "xmax",
      "value": 0.2
    },
    {
      "name": "xavg",
      "value": 0.15
    },
    {
      "name": "ymin",
      "value": -0.1
    },
    {
      "name": "ymax",
      "value": 0.2
    },
    {
      "name": "yavg",
      "value": 0.1
    },
    {
      "name": "zmin",
      "value": 0.01
    },
    {
      "name": "zmax",
      "value": 0.03
    },
    {
      "name": "zavg",
      "value": 0.02
    }
  ]
}
```

# Telemetry Properties

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                   |
| :-------------------------------- | :------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------- |
| [eventTimestamp](#eventtimestamp) | `string` | Required | cannot be null | [Telemetry](telemetry-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp") |
| [messageNumber](#messagenumber)   | `number` | Optional | cannot be null | [Telemetry](telemetry-properties-messagenumber.md "#/properties/messageNumber#/properties/messageNumber")    |
| [id](#id)                         | `string` | Required | cannot be null | [Telemetry](telemetry-properties-id.md "#/properties/id#/properties/id")                                     |
| [payloads](#payloads)             | `array`  | Required | cannot be null | [Telemetry](telemetry-properties-payloads.md "#/properties/payloads#/properties/payloads")                   |
| Additional Properties             | Any      | Optional | can be null    |                                                                                                              |

## eventTimestamp

ISO 8601, UTC.

`eventTimestamp`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Telemetry](telemetry-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp")

### eventTimestamp Type

`string`

## messageNumber

Optional. Sequence number, increased by one for each new message. Used to validate consistency in the data stream.

> Added in version 2.1

`messageNumber`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [Telemetry](telemetry-properties-messagenumber.md "#/properties/messageNumber#/properties/messageNumber")

### messageNumber Type

`number`

## id

Eight digit hex as defined above.

`id`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Telemetry](telemetry-properties-id.md "#/properties/id#/properties/id")

### id Type

`string`

## payloads

If FMS data or accelerometry, one payload per SPN. Else, one payload.

`payloads`

*   is required

*   Type: `object[]` ([Details](telemetry-properties-payloads-items.md))

*   cannot be null

*   defined in: [Telemetry](telemetry-properties-payloads.md "#/properties/payloads#/properties/payloads")

### payloads Type

`object[]` ([Details](telemetry-properties-payloads-items.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
