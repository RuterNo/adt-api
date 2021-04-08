# [v2.1](../../README.md) / [Operational information](README.md) / Current destination display 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/oi/current_destination_display/text```  | ```true``` | ```1```

# CurrentDestinationDisplay Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/current-destination-display.json
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                       |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [current-destination-display.json](../../schema/operational-information/current-destination-display.json "open original schema") |

## CurrentDestinationDisplay Type

`object` ([CurrentDestinationDisplay](current-destination-display.md))

## CurrentDestinationDisplay Examples

```json
{
  "name": "Tonsenhagen",
  "lineDesignation": "60"
}
```

# CurrentDestinationDisplay Properties

| Property                                        | Type     | Required | Nullable       | Defined by                                                                                                                                                           |
| :---------------------------------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [number](#number)                               | `number` | Optional | cannot be null | [CurrentDestinationDisplay](current-destination-display-properties-number.md "\#/properties/number#/properties/number")                                              |
| [name](#name)                                   | `string` | Required | cannot be null | [CurrentDestinationDisplay](current-destination-display-properties-name.md "\#/properties/name#/properties/name")                                                    |
| [alternativeText](#alternativetext)             | `string` | Optional | cannot be null | [CurrentDestinationDisplay](current-destination-display-properties-alternativetext.md "\#/properties/alternativeText#/properties/alternativeText")                   |
| [lineDesignation](#linedesignation)             | `string` | Optional | cannot be null | [CurrentDestinationDisplay](current-destination-display-properties-linedesignation.md "\#/properties/lineDesignation#/properties/lineDesignation")                   |
| [typeOfAlternativeText](#typeofalternativetext) | `string` | Optional | cannot be null | [CurrentDestinationDisplay](current-destination-display-properties-typeofalternativetext.md "\#/properties/typeOfAlternativeText#/properties/typeOfAlternativeText") |
| Additional Properties                           | Any      | Optional | can be null    |                                                                                                                                                                      |

## number

Optional. Numeric value representing the destination display text.


`number`

-   is optional
-   Type: `number`
-   cannot be null
-   defined in: [CurrentDestinationDisplay](current-destination-display-properties-number.md "\#/properties/number#/properties/number")

### number Type

`number`

## name

The name of the (primary) destination or a free text.


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [CurrentDestinationDisplay](current-destination-display-properties-name.md "\#/properties/name#/properties/name")

### name Type

`string`

## alternativeText

Optional. The name of the secondary destination or an alternative (free) text.


`alternativeText`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [CurrentDestinationDisplay](current-destination-display-properties-alternativetext.md "\#/properties/alternativeText#/properties/alternativeText")

### alternativeText Type

`string`

## lineDesignation

Optional. Displayed public line number or line code.


`lineDesignation`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [CurrentDestinationDisplay](current-destination-display-properties-linedesignation.md "\#/properties/lineDesignation#/properties/lineDesignation")

### lineDesignation Type

`string`

## typeOfAlternativeText

Optional. The purpose of the alternative text. Possible values in examples.


`typeOfAlternativeText`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [CurrentDestinationDisplay](current-destination-display-properties-typeofalternativetext.md "\#/properties/typeOfAlternativeText#/properties/typeOfAlternativeText")

### typeOfAlternativeText Type

`string`

### typeOfAlternativeText Examples

```json
"COUNT_DOWN_TO_DEPARTURE"
```

```json
"MESSAGE"
```

```json
"VIA"
```

```json
"END_STATION"
```

```json
"TRANSFER_AT_THIS_STOP"
```

```json
"CONTINUE_TO"
```

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
