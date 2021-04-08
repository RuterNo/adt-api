# [v2.1](../../README.md) / [Sensor](README.md) / Location 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/sensors/gnss/location```  | ```false``` | ```0```

# Location Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/sensor/location.json
```

Describes the GNSS navigation receiver feedback in metric format. The periodicity of updates to be expected should be described as number of seconds in configValue01 for this topic under topic ruter/{PTO}/{vehicleID}/mi/provider_clients//provided_topics

The GNSS type should be described in configValue11. Information about the used GNSS System. MixedGNSSTypes is used for receivers using multiple satellite constellations. Possible values: “GPS”, ”Glonass”, ”Galileo”, ”Beidou”, ”IRNSS”, ”Other”, ”DeadReckoning”, ”MixedGNSSTypes”

The GNSS coordinate system should be described in configValue12, at least if other than “WGS84”. Possible values: “GPS”, ”Glonass”, ”Galileo”, ”Beidou”, ”IRNSS”, ”Other”, ”DeadReckoning”, ”MixedGNSSTypes”. “MixedGNSSTypes” is used for receivers using multiple satellite constellations.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [location.json](../../schema/sensor/location.json "open original schema") |

## Location Type

`object` ([Location](location.md))

## Location Examples

```json
{
  "latitudeDegree": 59.251356,
  "longitudeDegree": 11.581231,
  "altitude": 124,
  "fixDateTime": "2017-11-30T23:45:52Z",
  "messageNumber": 12345,
  "speedOverGround": 15.3,
  "trackDegreeTrue": 324,
  "signalQuality": 1,
  "numberOfSatellites": 12,
  "hdop": 2.4
}
```

# Location Properties

| Property                                  | Type     | Required | Nullable       | Defined by                                                                                                              |
| :---------------------------------------- | -------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------- |
| [latitudeDegree](#latitudedegree)         | `number` | Required | cannot be null | [Location](location-properties-latitudedegree.md "\#/properties/latitudeDegree#/properties/latitudeDegree")             |
| [latitudeDirection](#latitudedirection)   | `string` | Optional | cannot be null | [Location](location-properties-latitudedirection.md "\#/properties/latitudeDirection#/properties/latitudeDirection")    |
| [longitudeDegree](#longitudedegree)       | `number` | Required | cannot be null | [Location](location-properties-longitudedegree.md "\#/properties/longitudeDegree#/properties/longitudeDegree")          |
| [longitudeDirection](#longitudedirection) | `string` | Optional | cannot be null | [Location](location-properties-longitudedirection.md "\#/properties/longitudeDirection#/properties/longitudeDirection") |
| [altitude](#altitude)                     | `number` | Required | cannot be null | [Location](location-properties-altitude.md "\#/properties/altitude#/properties/altitude")                               |
| [fixDateTime](#fixdatetime)               | `string` | Required | cannot be null | [Location](location-properties-fixdatetime.md "\#/properties/fixDateTime#/properties/fixDateTime")                      |
| [messageNumber](#messagenumber)           | `number` | Optional | cannot be null | [Location](location-properties-messagenumber.md "\#/properties/messageNumber#/properties/messageNumber")                |
| [speedOverGround](#speedoverground)       | `number` | Required | cannot be null | [Location](location-properties-speedoverground.md "\#/properties/speedOverGround#/properties/speedOverGround")          |
| [trackDegreeTrue](#trackdegreetrue)       | `number` | Required | cannot be null | [Location](location-properties-trackdegreetrue.md "\#/properties/trackDegreeTrue#/properties/trackDegreeTrue")          |
| [signalQuality](#signalquality)           | `number` | Required | cannot be null | [Location](location-properties-signalquality.md "\#/properties/signalQuality#/properties/signalQuality")                |
| [numberOfSatellites](#numberofsatellites) | `number` | Required | cannot be null | [Location](location-properties-numberofsatellites.md "\#/properties/numberOfSatellites#/properties/numberOfSatellites") |
| [hdop](#hdop)                             | `number` | Required | cannot be null | [Location](location-properties-hdop.md "\#/properties/hdop#/properties/hdop")                                           |
| Additional Properties                     | Any      | Optional | can be null    |                                                                                                                         |

## latitudeDegree

Latitude coordinate in decimal degrees.


`latitudeDegree`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-latitudedegree.md "\#/properties/latitudeDegree#/properties/latitudeDegree")

### latitudeDegree Type

`number`

## latitudeDirection

Optional. Latitude direction (“N” or “S”).


`latitudeDirection`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [Location](location-properties-latitudedirection.md "\#/properties/latitudeDirection#/properties/latitudeDirection")

### latitudeDirection Type

`string`

## longitudeDegree

Longitude coordinate in decimal degrees.


`longitudeDegree`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-longitudedegree.md "\#/properties/longitudeDegree#/properties/longitudeDegree")

### longitudeDegree Type

`number`

## longitudeDirection

Optional. Longitude direction (“W” or “E”).


`longitudeDirection`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [Location](location-properties-longitudedirection.md "\#/properties/longitudeDirection#/properties/longitudeDirection")

### longitudeDirection Type

`string`

## altitude

Altitude value (m) above mean sea level.


`altitude`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-altitude.md "\#/properties/altitude#/properties/altitude")

### altitude Type

`number`

## fixDateTime

ISO 8601. Reflects the UTC time provided by the GNSS equipment for position fix. This is the point in time the location applies to.


`fixDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [Location](location-properties-fixdatetime.md "\#/properties/fixDateTime#/properties/fixDateTime")

### fixDateTime Type

`string`

## messageNumber

Optional. Sequence number, increased by one for each new message. Used to validate consistency in the data stream.


> Added in version 2.1
>

`messageNumber`

-   is optional
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-messagenumber.md "\#/properties/messageNumber#/properties/messageNumber")

### messageNumber Type

`number`

## speedOverGround

GNSS based speed over ground (m/s).


`speedOverGround`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-speedoverground.md "\#/properties/speedOverGround#/properties/speedOverGround")

### speedOverGround Type

`number`

## trackDegreeTrue

Direction of travel in relation to the geographical North Pole (0-360 degrees).


`trackDegreeTrue`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-trackdegreetrue.md "\#/properties/trackDegreeTrue#/properties/trackDegreeTrue")

### trackDegreeTrue Type

`number`

## signalQuality

GPS quality indicator. 0 - Fix not available. 1 - GPS fix. 2 - Differential GPS fix. 3 = PPS fix. 4 = Real Time Kinematic. 5 = Float RTK. 6 = Estimated (dead reckoning). 7 = Manual input mode. 8 = Simulation mode


`signalQuality`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-signalquality.md "\#/properties/signalQuality#/properties/signalQuality")

### signalQuality Type

`number`

## numberOfSatellites

Number of satellites used.


`numberOfSatellites`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-numberofsatellites.md "\#/properties/numberOfSatellites#/properties/numberOfSatellites")

### numberOfSatellites Type

`number`

## hdop

Value of precision in horizontal dilution.


`hdop`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [Location](location-properties-hdop.md "\#/properties/hdop#/properties/hdop")

### hdop Type

`number`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
