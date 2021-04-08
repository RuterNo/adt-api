# [v2.1](../../README.md) / [Extended information](README.md) / Audio message 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/ei/audio_message```  | ```false``` | ```0```

# AudioMessage Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/extended-information/audio-message.json
```

This topic provides an audio message intended for passengers onboard the vehicle that should be played on speaker(s) defined in the speaker property of the payload.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                        |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [audio-message.json](../../schema/extended-information/audio-message.json "open original schema") |

## AudioMessage Type

`object` ([AudioMessage](audio-message.md))

## AudioMessage Examples

```json
{
  "eventDateTime": "2018-11-13T11:40:02.749Z",
  "expiryDateTime": "2018-11-13T08:40:32.249Z",
  "preferredStartDateTime": "2018-11-13T08:39:32.749Z",
  "ref": "RUT:StopPlace:03012453",
  "audio": [
    {
      "encoding": "OPUS",
      "contentUrl": "\\soundserver\\path\\to\\file",
      "speaker": "INTERNAL",
      "volume": 70
    },
    {
      "encoding": "MP3",
      "content": "SUQzBAAAAAAAI1RTU0UAAAAPAAADTGF2ZjU3...",
      "speaker": "INTERNAL",
      "volume": 70
    }
  ]
}
```

# AudioMessage Properties

| Property                                          | Type          | Required | Nullable       | Defined by                                                                                                                                   |
| :------------------------------------------------ | ------------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| [eventDateTime](#eventdatetime)                   | `string`      | Required | cannot be null | [AudioMessage](audio-message-properties-eventdatetime.md "\#/properties/eventDateTime#/properties/eventDateTime")                            |
| [expiryDateTime](#expirydatetime)                 | `string`      | Required | cannot be null | [AudioMessage](audio-message-properties-expirydatetime.md "\#/properties/expiryDateTime#/properties/expiryDateTime")                         |
| [preferredStartDateTime](#preferredstartdatetime) | `string`      | Required | cannot be null | [AudioMessage](audio-message-properties-preferredstartdatetime.md "\#/properties/preferredStartDateTime#/properties/preferredStartDateTime") |
| [ref](#ref)                                       | Not specified | Required | cannot be null | [AudioMessage](audio-message-properties-ref.md "\#/properties/ref#/properties/ref")                                                          |
| [audio](#audio)                                   | `array`       | Required | cannot be null | [AudioMessage](audio-message-properties-audio.md "\#/properties/audio#/properties/audio")                                                    |
| Additional Properties                             | Any           | Optional | can be null    |                                                                                                                                              |

## eventDateTime

ISO 8601, UTC


`eventDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-eventdatetime.md "\#/properties/eventDateTime#/properties/eventDateTime")

### eventDateTime Type

`string`

## expiryDateTime

Do not present this information after this time. ISO 8601, UTC


`expiryDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-expirydatetime.md "\#/properties/expiryDateTime#/properties/expiryDateTime")

### expiryDateTime Type

`string`

## preferredStartDateTime

ISO 8601, UTC


`preferredStartDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-preferredstartdatetime.md "\#/properties/preferredStartDateTime#/properties/preferredStartDateTime")

### preferredStartDateTime Type

`string`

## ref




`ref`

-   is required
-   Type: unknown
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-ref.md "\#/properties/ref#/properties/ref")

### ref Type

unknown

## audio




`audio`

-   is required
-   Type: `object[]` ([audio](audio-message-properties-audio-audio.md))
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-audio.md "\#/properties/audio#/properties/audio")

### audio Type

`object[]` ([audio](audio-message-properties-audio-audio.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
