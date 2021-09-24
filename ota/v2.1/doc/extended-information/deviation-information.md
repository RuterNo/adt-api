# [v2.1](../../README.md) / [Extended information](README.md) / Deviation information 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/ei/deviation_information/```  | ```true``` | ```1```

# DeviationInformation Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/extended-information/deviation-information.json
```

This topic provides an adapted selection of deviation and incident information that is relevant for passengers onboard this vehicle in scope of what the vehicle is currently doing and where it is on the current vehicle journey. The information is provided in the form of a list of situation messages. This topic should be blanked (provided with empty content) if there are no relevant situation messages. As an added precaution an expiry timestamp is included to assure that outdated information is not presented.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [deviation-information.json](../../schema/extended-information/deviation-information.json "open original schema") |

## DeviationInformation Type

`object` ([DeviationInformation](deviation-information.md))

## DeviationInformation Examples

```json
{
  "expiryDateTime": "2017-10-31T12:45:50Z",
  "heading": "Deviation information",
  "displayDurationSeconds": 7,
  "situationMessages": [
    {
      "heading": "Metro breakdown",
      "body": "Metro-line 17 is temporarily out of operation due to a power outage."
    },
    {
      "heading": "Metro breakdown",
      "body": "Metro-line 18 is temporarily out of operation due to a power outage."
    }
  ]
}
```

# DeviationInformation Properties

| Property                                          | Type     | Required | Nullable       | Defined by                                                                                                                                                  |
| :------------------------------------------------ | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [expiryDateTime](#expirydatetime)                 | `string` | Required | cannot be null | [DeviationInformation](deviation-information-properties-expirydatetime.md "#/properties/expiryDateTime#/properties/expiryDateTime")                         |
| [heading](#heading)                               | `string` | Optional | cannot be null | [DeviationInformation](deviation-information-properties-heading.md "#/properties/heading#/properties/heading")                                              |
| [displayDurationSeconds](#displaydurationseconds) | `number` | Optional | cannot be null | [DeviationInformation](deviation-information-properties-displaydurationseconds.md "#/properties/displayDurationSeconds#/properties/displayDurationSeconds") |
| [message](#message)                               | `string` | Optional | cannot be null | [DeviationInformation](deviation-information-properties-message.md "#/properties/message#/properties/message")                                              |
| [situationMessages](#situationmessages)           | `array`  | Required | cannot be null | [DeviationInformation](deviation-information-properties-situation-messages.md "#/properties/situationMessages#/properties/situationMessages")               |
| Additional Properties                             | Any      | Optional | can be null    |                                                                                                                                                             |

## expiryDateTime

Do not present this information after this time. ISO 8601, UTC

`expiryDateTime`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DeviationInformation](deviation-information-properties-expirydatetime.md "#/properties/expiryDateTime#/properties/expiryDateTime")

### expiryDateTime Type

`string`

## heading

Optional. The heading to be displayed.

`heading`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [DeviationInformation](deviation-information-properties-heading.md "#/properties/heading#/properties/heading")

### heading Type

`string`

### heading Examples

```json
"Deviation information"
```

## displayDurationSeconds

Optional. The recommended number of seconds the deviation information shall be presented. This value depends on the number of items and content type, reflecting the time it takes for a passenger to read it.

`displayDurationSeconds`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [DeviationInformation](deviation-information-properties-displaydurationseconds.md "#/properties/displayDurationSeconds#/properties/displayDurationSeconds")

### displayDurationSeconds Type

`number`

## message

Optional. Text to be presented instead of situation messages when no deviation information is available due to technical problems or similar.

`message`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [DeviationInformation](deviation-information-properties-message.md "#/properties/message#/properties/message")

### message Type

`string`

### message Examples

```json
"Due to technical problems, deviation information cannot be displayed at the moment."
```

## situationMessages

A list of situation messages that are currently relevant to the passengers onboard the vehicle at this point in the vehicle journey.

`situationMessages`

*   is required

*   Type: `object[]` ([Situation Message](deviation-information-properties-situation-messages-situation-message.md))

*   cannot be null

*   defined in: [DeviationInformation](deviation-information-properties-situation-messages.md "#/properties/situationMessages#/properties/situationMessages")

### situationMessages Type

`object[]` ([Situation Message](deviation-information-properties-situation-messages-situation-message.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
