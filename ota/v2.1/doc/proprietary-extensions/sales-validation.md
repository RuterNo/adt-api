# [v2.1](../../README.md) / [Proprietary extensions](README.md) / Sales validation 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/pe/sales_validation```  | ```false``` | ```1```

# SalesValidation Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/proprietary-extensions/sales-validation.json
```

Submits status of RuterSales application in the vehicle. The status can be submitted both at a periodic interval and when a ticket is sold or validated.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [sales-validation.json](../../schema/proprietary-extensions/sales-validation.json "open original schema") |

## SalesValidation Type

`object` ([SalesValidation](sales-validation.md))

## SalesValidation Examples

```json
{
  "validationOk": "true",
  "status": "OK",
  "atDateTime": "2020-10-31T12:45:50Z"
}
```

# SalesValidation Properties

| Property                                  | Type     | Required | Nullable       | Defined by                                                                                                                            |
| :---------------------------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------ |
| [status](#status)                         | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-status.md "#/properties/status#/properties/status")                                     |
| [validationOk](#validationok)             | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-validationok.md "#/properties/validationOk#/properties/validationOk")                   |
| [validationText](#validationtext)         | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-validationtext.md "#/properties/validationText#/properties/validationText")             |
| [validationColor](#validationcolor)       | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-validationcolor.md "#/properties/validationColor#/properties/validationColor")          |
| [validationSound](#validationsound)       | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-validationsound.md "#/properties/validationSound#/properties/validationSound")          |
| [nfcReaderConnected](#nfcreaderconnected) | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-nfcreaderconnected.md "#/properties/nfcReaderConnected#/properties/nfcReaderConnected") |
| [printerConnected](#printerconnected)     | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-printerconnected.md "#/properties/printerConnected#/properties/printerConnected")       |
| [printerStatus](#printerstatus)           | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-printerstatus.md "#/properties/printerStatus#/properties/printerStatus")                |
| [nodAvailable](#nodavailable)             | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-nodavailable.md "#/properties/nodAvailable#/properties/nodAvailable")                   |
| [sapiAvailable](#sapiavailable)           | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-sapiavailable.md "#/properties/sapiAvailable#/properties/sapiAvailable")                |
| [loggedIn](#loggedin)                     | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-loggedin.md "#/properties/loggedIn#/properties/loggedIn")                               |
| [atDateTime](#atdatetime)                 | `string` | Optional | cannot be null | [SalesValidation](sales-validation-properties-atdatetime.md "#/properties/atDateTime#/properties/atDateTime")                         |
| Additional Properties                     | Any      | Optional | can be null    |                                                                                                                                       |

## status

Status

`status`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-status.md "#/properties/status#/properties/status")

### status Type

`string`

### status Examples

```json
"OK"
```

```json
"ERROR"
```

## validationOk

True if validation is positive

`validationOk`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-validationok.md "#/properties/validationOk#/properties/validationOk")

### validationOk Type

`string`

### validationOk Examples

```json
"true"
```

```json
"false"
```

## validationText

Text result from NOD

`validationText`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-validationtext.md "#/properties/validationText#/properties/validationText")

### validationText Type

`string`

## validationColor

Color result from NOD

`validationColor`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-validationcolor.md "#/properties/validationColor#/properties/validationColor")

### validationColor Type

`string`

## validationSound

Sound result from NOD

`validationSound`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-validationsound.md "#/properties/validationSound#/properties/validationSound")

### validationSound Type

`string`

## nfcReaderConnected

True if NFC reader is connected

`nfcReaderConnected`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-nfcreaderconnected.md "#/properties/nfcReaderConnected#/properties/nfcReaderConnected")

### nfcReaderConnected Type

`string`

### nfcReaderConnected Examples

```json
"true"
```

```json
"false"
```

## printerConnected

True if last connection attempt/print was successful

`printerConnected`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-printerconnected.md "#/properties/printerConnected#/properties/printerConnected")

### printerConnected Type

`string`

### printerConnected Examples

```json
"true"
```

```json
"false"
```

## printerStatus

Latest status from printer if printerConnected is false

`printerStatus`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-printerstatus.md "#/properties/printerStatus#/properties/printerStatus")

### printerStatus Type

`string`

## nodAvailable

True if app is able to reach NOD

`nodAvailable`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-nodavailable.md "#/properties/nodAvailable#/properties/nodAvailable")

### nodAvailable Type

`string`

### nodAvailable Examples

```json
"true"
```

```json
"false"
```

## sapiAvailable

True if app is able to reach sapi

`sapiAvailable`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-sapiavailable.md "#/properties/sapiAvailable#/properties/sapiAvailable")

### sapiAvailable Type

`string`

### sapiAvailable Examples

```json
"true"
```

```json
"false"
```

## loggedIn

True if a user currently is logged in

`loggedIn`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-loggedin.md "#/properties/loggedIn#/properties/loggedIn")

### loggedIn Type

`string`

### loggedIn Examples

```json
"true"
```

```json
"false"
```

## atDateTime

When the ticket is sold/validated or the timestamp for periodic reporting e.g. 1/min.

`atDateTime`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesValidation](sales-validation-properties-atdatetime.md "#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
