# [v2.0](../../README.md) / [Sensor](README.md) / Clock 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```sensors/clock```  | ```false``` | ```0```

# Clock Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/sensor/clock.json
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                          |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [clock.json](../../schema/sensor/clock.json "open original schema") |

## Clock Type

`object` ([Clock](clock.md))

## Clock Examples

```json
{
  "localTimeZoneDate": "2017-12-01",
  "localTimeZoneTime": "00:45:52",
  "atDateTime": "2017-11-30T23:45:52.006Z"
}
```

# Clock Properties

| Property                                | Type     | Required | Nullable       | Defined by                                                                                                     |
| :-------------------------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------- |
| [localTimeZoneDate](#localtimezonedate) | `string` | Required | cannot be null | [Clock](clock-properties-localtimezonedate.md "\#/properties/localTimeZoneDate#/properties/localTimeZoneDate") |
| [localTimeZoneTime](#localtimezonetime) | `string` | Required | cannot be null | [Clock](clock-properties-localtimezonetime.md "\#/properties/localTimeZoneTime#/properties/localTimeZoneTime") |
| [atDateTime](#atdatetime)               | `string` | Required | cannot be null | [Clock](clock-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")                      |
| Additional Properties                   | Any      | Optional | can be null    |                                                                                                                |

## localTimeZoneDate

Date formatted as YYYY-MM-DD where YYYY = year MM = month [01..12] DD = day [01..31].


`localTimeZoneDate`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [Clock](clock-properties-localtimezonedate.md "\#/properties/localTimeZoneDate#/properties/localTimeZoneDate")

### localTimeZoneDate Type

`string`

## localTimeZoneTime

Time formatted as hh:mm:ss where hh = hour [00..23] mm = minute [00..59] ss = seconds [00..59].


`localTimeZoneTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [Clock](clock-properties-localtimezonetime.md "\#/properties/localTimeZoneTime#/properties/localTimeZoneTime")

### localTimeZoneTime Type

`string`

## atDateTime

ISO 8601. Reflects the UTC time when the information was provided.


`atDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [Clock](clock-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
