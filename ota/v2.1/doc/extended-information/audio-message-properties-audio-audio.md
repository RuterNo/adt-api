# audio Schema

```txt
#/properties/audio#/properties/audio/items
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                          |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | --------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [audio-message.json\*](../../schema/extended-information/audio-message.json "open original schema") |

## items Type

`object` ([audio](audio-message-properties-audio-audio.md))

# audio Properties

| Property                  | Type     | Required | Nullable       | Defined by                                                                                                                                        |
| :------------------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| [encoding](#encoding)     | `string` | Optional | cannot be null | [AudioMessage](audio-message-properties-audio-audio-properties-encoding.md "\#/properties/audio#/properties/audio/items/properties/encoding")     |
| [content](#content)       | `string` | Optional | cannot be null | [AudioMessage](audio-message-properties-audio-audio-properties-content.md "\#/properties/audio#/properties/audio/items/properties/content")       |
| [contentURL](#contenturl) | `string` | Optional | cannot be null | [AudioMessage](audio-message-properties-audio-audio-properties-contenturl.md "\#/properties/audio#/properties/audio/items/properties/contentURL") |
| [speaker](#speaker)       | `string` | Required | cannot be null | [AudioMessage](audio-message-properties-audio-audio-properties-speaker.md "\#/properties/audio#/properties/audio/items/properties/speaker")       |
| [volume](#volume)         | `number` | Required | cannot be null | [AudioMessage](audio-message-properties-audio-audio-properties-volume.md "\#/properties/audio#/properties/audio/items/properties/volume")         |

## encoding

Optional. Audio message encoding


`encoding`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-audio-audio-properties-encoding.md "\#/properties/audio#/properties/audio/items/properties/encoding")

### encoding Type

`string`

### encoding Examples

```json
"MP3"
```

```json
"OPUS"
```

## content

Optional. BASE64 encoded binary data. Do not use if contentURL is defined


`content`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-audio-audio-properties-content.md "\#/properties/audio#/properties/audio/items/properties/content")

### content Type

`string`

## contentURL

Optional. Location of content. Do not use if content is defined.


`contentURL`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-audio-audio-properties-contenturl.md "\#/properties/audio#/properties/audio/items/properties/contentURL")

### contentURL Type

`string`

## speaker

Speaker the audio is intended for


`speaker`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-audio-audio-properties-speaker.md "\#/properties/audio#/properties/audio/items/properties/speaker")

### speaker Type

`string`

### speaker Examples

```json
"INTERNAL"
```

```json
"EXTERNAL"
```

```json
"DRIVER"
```

## volume

Volume in dB


`volume`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [AudioMessage](audio-message-properties-audio-audio-properties-volume.md "\#/properties/audio#/properties/audio/items/properties/volume")

### volume Type

`number`
