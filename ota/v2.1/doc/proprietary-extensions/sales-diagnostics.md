# [v2.1](../../README.md) / [Proprietary extensions](README.md) / Sales diagnostics 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/pe/sales/diagnostics```  | ```false``` | ```1```

# SalesDiagnostics Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/proprietary-extensions/sales-diagnostics.json
```

Health status for the Sales application "Ruter Salg" and it peripheral connections. Diagnostics performed and reuslts sent before every stop.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                  |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [sales-diagnostics.json](../../schema/proprietary-extensions/sales-diagnostics.json "open original schema") |

## SalesDiagnostics Type

`object` ([SalesDiagnostics](sales-diagnostics.md))

## SalesDiagnostics Examples

```json
{
  "eventTimestamp": "2020-04-27T12:56:47.110Z",
  "nfcReaderConnected": true,
  "printerConnected": false,
  "printerStatus": "Deksel er åpnet",
  "nodAvailable": true,
  "sapiAvailable": true,
  "loggedIn": true,
  "journeyRef": "42911-2020-05-25T16:42:00+02:00",
  "stopPlaceId": "NSR:StopPlace:59734"
}
```

# SalesDiagnostics Properties

| Property                                  | Type      | Required | Nullable       | Defined by                                                                                                                              |
| :---------------------------------------- | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| [eventTimestamp](#eventtimestamp)         | `string`  | Required | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp")             |
| [nfcReaderConnected](#nfcreaderconnected) | `boolean` | Required | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-nfcreaderconnected.md "#/properties/nfcReaderConnected#/properties/nfcReaderConnected") |
| [printerConnected](#printerconnected)     | `boolean` | Required | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-printerconnected.md "#/properties/printerConnected#/properties/printerConnected")       |
| [printerStatus](#printerstatus)           | `string`  | Optional | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-printerstatus.md "#/properties/printerStatus#/properties/printerStatus")                |
| [nodAvailable](#nodavailable)             | `boolean` | Required | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-nodavailable.md "#/properties/nodAvailable#/properties/nodAvailable")                   |
| [sapiAvailable](#sapiavailable)           | `boolean` | Required | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-sapiavailable.md "#/properties/sapiAvailable#/properties/sapiAvailable")                |
| [loggedIn](#loggedin)                     | `boolean` | Required | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-loggedin.md "#/properties/loggedIn#/properties/loggedIn")                               |
| [journeyRef](#journeyref)                 | `string`  | Optional | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-journeyref.md "#/properties/journeyRef#/properties/journeyRef")                         |
| [stopPlaceId](#stopplaceid)               | `string`  | Optional | cannot be null | [SalesDiagnostics](sales-diagnostics-properties-stopplaceid.md "#/properties/stopPlaceId#/properties/stopPlaceId")                      |
| Additional Properties                     | Any       | Optional | can be null    |                                                                                                                                         |

## eventTimestamp

ISO 8601, UTC. The time of this diagnostics message generation

`eventTimestamp`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp")

### eventTimestamp Type

`string`

### eventTimestamp Constraints

**unknown format**: the value of this string must follow the format: `string`

## nfcReaderConnected

True if the NFC reader is discovered and connected by the app

`nfcReaderConnected`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-nfcreaderconnected.md "#/properties/nfcReaderConnected#/properties/nfcReaderConnected")

### nfcReaderConnected Type

`boolean`

## printerConnected

True if the printer is discovered and connected, and if the previous communication with the printer was a print operation the print was a success

`printerConnected`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-printerconnected.md "#/properties/printerConnected#/properties/printerConnected")

### printerConnected Type

`boolean`

## printerStatus

Optional. If printerConnected is false, printerStatus might contain last errorMessage from printer if available, or error message from the sales device if unavailable

`printerStatus`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-printerstatus.md "#/properties/printerStatus#/properties/printerStatus")

### printerStatus Type

`string`

## nodAvailable

True if the app can contact the NOD backend

`nodAvailable`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-nodavailable.md "#/properties/nodAvailable#/properties/nodAvailable")

### nodAvailable Type

`boolean`

## sapiAvailable

True if the app can contact the SAPI backend

`sapiAvailable`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-sapiavailable.md "#/properties/sapiAvailable#/properties/sapiAvailable")

### sapiAvailable Type

`boolean`

## loggedIn

True if a user is logged into the app

`loggedIn`

*   is required

*   Type: `boolean`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-loggedin.md "#/properties/loggedIn#/properties/loggedIn")

### loggedIn Type

`boolean`

## journeyRef

Last received journeyRef. Obtained from last received Journey message.

`journeyRef`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-journeyref.md "#/properties/journeyRef#/properties/journeyRef")

### journeyRef Type

`string`

## stopPlaceId

Last received stopPlaceId. Obtained from last received NextStop message with a valid Ruter zone

`stopPlaceId`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [SalesDiagnostics](sales-diagnostics-properties-stopplaceid.md "#/properties/stopPlaceId#/properties/stopPlaceId")

### stopPlaceId Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
