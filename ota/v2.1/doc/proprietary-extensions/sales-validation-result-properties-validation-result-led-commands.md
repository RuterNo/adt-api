# Validation result LED commands Schema

```txt
#/properties/ledCommand#/properties/ledCommand
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                               |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :----------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [sales-validation-result.json*](../../schema/proprietary-extensions/sales-validation-result.json "open original schema") |

## ledCommand Type

`object` ([Validation result LED commands](sales-validation-result-properties-validation-result-led-commands.md))

# ledCommand Properties

| Property              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                 |
| :-------------------- | :-------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [color](#color)       | `string`  | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-color.md "#/properties/ledCommand/properties/color#/properties/ledCommand/properties/color")          |
| [duration](#duration) | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-duration.md "#/properties/ledCommand/properties/duration#/properties/ledCommand/properties/duration") |
| [pause](#pause)       | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-pause.md "#/properties/ledCommand/properties/pause#/properties/ledCommand/properties/pause")          |
| [repeat](#repeat)     | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-repeat.md "#/properties/ledCommand/properties/repeat#/properties/ledCommand/properties/repeat")       |

## color

Color to be displayed ("red" and "green" are the possible values as of now)

`color`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-color.md "#/properties/ledCommand/properties/color#/properties/ledCommand/properties/color")

### color Type

`string`

### color Examples

```json
"red"
```

```json
"green"
```

## duration

Duration in ms the color should be displayed

`duration`

*   is required

*   Type: `integer`

*   cannot be null

*   defined in: [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-duration.md "#/properties/ledCommand/properties/duration#/properties/ledCommand/properties/duration")

### duration Type

`integer`

## pause

How long the pause should be between each time the color is displayed

`pause`

*   is required

*   Type: `integer`

*   cannot be null

*   defined in: [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-pause.md "#/properties/ledCommand/properties/pause#/properties/ledCommand/properties/pause")

### pause Type

`integer`

## repeat

The number of times the color should be displayed

`repeat`

*   is required

*   Type: `integer`

*   cannot be null

*   defined in: [SalesValidationResult](sales-validation-result-properties-validation-result-led-commands-properties-repeat.md "#/properties/ledCommand/properties/repeat#/properties/ledCommand/properties/repeat")

### repeat Type

`integer`
