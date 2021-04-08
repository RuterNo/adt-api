# Untitled object in SalesValidationResult Schema

```txt
#/properties/buzzerCommand#/properties/buzzerCommand
```

Buzzer sound result of validation


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [sales-validation-result.json\*](../../schema/proprietary-extensions/sales-validation-result.json "open original schema") |

## buzzerCommand Type

`object` ([Details](sales-validation-result-properties-buzzercommand.md))

# undefined Properties

| Property                | Type      | Required | Nullable       | Defined by                                                                                                                                                                                          |
| :---------------------- | --------- | -------- | -------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [duration](#duration)   | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-duration.md "\#/properties/buzzerCommand/properties/duration#/properties/buzzerCommand/properties/duration")    |
| [frequency](#frequency) | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-frequency.md "\#/properties/buzzerCommand/properties/frequency#/properties/buzzerCommand/properties/frequency") |
| [pause](#pause)         | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-pause.md "\#/properties/buzzerCommand/properties/pause#/properties/buzzerCommand/properties/pause")             |
| [repeat](#repeat)       | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-repeat.md "\#/properties/buzzerCommand/properties/repeat#/properties/buzzerCommand/properties/repeat")          |

## duration

The duration of each buzz in ms


`duration`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-duration.md "\#/properties/buzzerCommand/properties/duration#/properties/buzzerCommand/properties/duration")

### duration Type

`integer`

## frequency

Frequency to be used for buzzes


`frequency`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-frequency.md "\#/properties/buzzerCommand/properties/frequency#/properties/buzzerCommand/properties/frequency")

### frequency Type

`integer`

## pause

Pause between each buzz in ms


`pause`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-pause.md "\#/properties/buzzerCommand/properties/pause#/properties/buzzerCommand/properties/pause")

### pause Type

`integer`

## repeat

The number of times the buzz should be repeated


`repeat`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesValidationResult](sales-validation-result-properties-buzzercommand-properties-repeat.md "\#/properties/buzzerCommand/properties/repeat#/properties/buzzerCommand/properties/repeat")

### repeat Type

`integer`
