# [v2.0](../../README.md) / [Extended information](README.md) / Transfer information 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/ei/expected_call/transfer_information```  | ```true``` | ```1```

# TransferInformation Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/extended-information/transfer-information.json
```

This topic provides an adapted selection of real time information describing connecting lines at the current or the coming stop that passengers onboard this vehicle could transfer to. The information is provided in the form of a list of possible transfer options at the next stop.

 This topic should be blanked (provided with empty content) when there is no relevant information to display.

 As an added precaution an expiry timestamp is included to assure that outdated information is not presented.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                      |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | --------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [transfer-information.json](../../schema/extended-information/transfer-information.json "open original schema") |

## TransferInformation Type

`object` ([TransferInformation](transfer-information.md))

## TransferInformation Examples

```json
{
  "expiryDateTime": "2017-10-31T12:45:50Z",
  "heading": "Departures from Slussen",
  "displayDurationSeconds": 10,
  "transferOptions": [
    {
      "transportMode": "BUS",
      "lineDesignation": "76",
      "destinationDisplayName": "Ropsten",
      "stopPointDesignation": "B",
      "presentedDepartureTimes": [
        "3 min",
        "11 min"
      ]
    },
    {
      "transportMode": "BUS",
      "lineDesignation": "55",
      "destinationDisplayName": "Sofia",
      "stopPointDesignation": "C",
      "presentedDepartureTimes": [
        "Now",
        "19 min"
      ]
    }
  ]
}
```

# TransferInformation Properties

| Property                                          | Type     | Required | Nullable       | Defined by                                                                                                                                                 |
| :------------------------------------------------ | -------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [expiryDateTime](#expirydatetime)                 | `string` | Required | cannot be null | [TransferInformation](transfer-information-properties-expirydatetime.md "\#/properties/expiryDateTime#/properties/expiryDateTime")                         |
| [heading](#heading)                               | `string` | Optional | cannot be null | [TransferInformation](transfer-information-properties-heading.md "\#/properties/heading#/properties/heading")                                              |
| [displayDurationSeconds](#displaydurationseconds) | `number` | Optional | cannot be null | [TransferInformation](transfer-information-properties-displaydurationseconds.md "\#/properties/displayDurationSeconds#/properties/displayDurationSeconds") |
| [message](#message)                               | `string` | Optional | cannot be null | [TransferInformation](transfer-information-properties-message.md "\#/properties/message#/properties/message")                                              |
| [transferOptions](#transferoptions)               | `array`  | Required | cannot be null | [TransferInformation](transfer-information-properties-transferoptions.md "\#/properties/transferOptions#/properties/transferOptions")                      |
| Additional Properties                             | Any      | Optional | can be null    |                                                                                                                                                            |

## expiryDateTime

Do not present this information after this time. ISO 8601, UTC


`expiryDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-expirydatetime.md "\#/properties/expiryDateTime#/properties/expiryDateTime")

### expiryDateTime Type

`string`

## heading

Optional. The heading to be displayed.


`heading`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-heading.md "\#/properties/heading#/properties/heading")

### heading Type

`string`

### heading Examples

```json
"Next departures from City Centre"
```

## displayDurationSeconds

Optional. The recommended number of seconds the transfer options shall be presented. This value depends on the number of items and content type, reflecting the time it takes for a passenger to read it.


`displayDurationSeconds`

-   is optional
-   Type: `number`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-displaydurationseconds.md "\#/properties/displayDurationSeconds#/properties/displayDurationSeconds")

### displayDurationSeconds Type

`number`

## message

Optional. Text to be presented when no transfer option information is available for a stop where transfer options usually are presented.


`message`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-message.md "\#/properties/message#/properties/message")

### message Type

`string`

### message Examples

```json
"No departures from City Centre within the next 20 minutes"
```

```json
"Due to technical problems, departures cannot be displayed at the moment."
```

## transferOptions

A list of Transfer Options that are currently relevant to the passengers onboard the vehicle at this point in the vehicle journey.


`transferOptions`

-   is required
-   Type: `object[]` ([transferOption](transfer-information-properties-transferoptions-transferoption.md))
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-transferoptions.md "\#/properties/transferOptions#/properties/transferOptions")

### transferOptions Type

`object[]` ([transferOption](transfer-information-properties-transferoptions-transferoption.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
