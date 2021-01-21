# [v2.0](../../README.md) / [Extended information](README.md) / Due information 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/ei/expected_call/due_information/```  | ```false``` | ```0```

# DueInformation Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/extended-information/due-information.json
```

This topic provides an adapted text indicating that the vehicle is about to arrive at a stop according to what the coordinating application has concluded.

 This could optionally be based on information provided in real-time from a back-office AVMS. However, if contact is lost with the back-office for more than a configured duration the information should be based on local information.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                            |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ----------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [due-information.json](../../schema/extended-information/due-information.json "open original schema") |

## DueInformation Type

`object` ([DueInformation](due-information.md))

## DueInformation Examples

```json
{
  "expiryDateTime": "2017-10-31T12:45:50Z",
  "heading": "Arriving at",
  "body": "Broparken"
}
```

# DueInformation Properties

| Property                                          | Type     | Required | Nullable       | Defined by                                                                                                                                       |
| :------------------------------------------------ | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------------------------- |
| [expiryDateTime](#expirydatetime)                 | `string` | Required | cannot be null | [DueInformation](due-information-properties-expirydatetime.md "\#/properties/expiryDateTime#/properties/expiryDateTime")                         |
| [heading](#heading)                               | `string` | Optional | cannot be null | [DueInformation](due-information-properties-heading.md "\#/properties/heading#/properties/heading")                                              |
| [body](#body)                                     | `string` | Required | cannot be null | [DueInformation](due-information-properties-body.md "\#/properties/body#/properties/body")                                                       |
| [displayDurationSeconds](#displaydurationseconds) | `number` | Optional | cannot be null | [DueInformation](due-information-properties-displaydurationseconds.md "\#/properties/displayDurationSeconds#/properties/displayDurationSeconds") |
| Additional Properties                             | Any      | Optional | can be null    |                                                                                                                                                  |

## expiryDateTime

Do not present this information after this time. ISO 8601, UTC


`expiryDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [DueInformation](due-information-properties-expirydatetime.md "\#/properties/expiryDateTime#/properties/expiryDateTime")

### expiryDateTime Type

`string`

## heading

Optional. The heading to be displayed.


`heading`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [DueInformation](due-information-properties-heading.md "\#/properties/heading#/properties/heading")

### heading Type

`string`

### heading Examples

```json
"Arriving at"
```

## body

The stop that the bus is approaching.


`body`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [DueInformation](due-information-properties-body.md "\#/properties/body#/properties/body")

### body Type

`string`

### body Examples

```json
"Broparken"
```

## displayDurationSeconds

Optional. The recommended number of seconds the due information shall be presented. This value depends on the number of items and content type, reflecting the time it takes for a passenger to read it.


`displayDurationSeconds`

-   is optional
-   Type: `number`
-   cannot be null
-   defined in: [DueInformation](due-information-properties-displaydurationseconds.md "\#/properties/displayDurationSeconds#/properties/displayDurationSeconds")

### displayDurationSeconds Type

`number`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
