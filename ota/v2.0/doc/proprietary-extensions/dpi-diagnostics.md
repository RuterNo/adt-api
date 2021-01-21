# [v2.0](../../README.md) / [Proprietary extensions](README.md) / Dpi diagnostics 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/pe/dpi_diagnostics```  | ```false``` | ```1```

# DPIDiagnostics Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/proprietary-extensions/dpi-diagnostics.json
```

It is expected that the DPI application itself will produce diagnostic messages. The payload is defined as an object with no structure to provide flexibility.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                              |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [dpi-diagnostics.json](../../schema/proprietary-extensions/dpi-diagnostics.json "open original schema") |

## DPIDiagnostics Type

`object` ([DPIDiagnostics](dpi-diagnostics.md))

## DPIDiagnostics Examples

```json
{
  "eventTimestamp": "2018-10-31T12:45:50Z",
  "screenId": "ad71dba8-c881-11e8-a8d5-f2801f1b9fd1",
  "type": "STATUS",
  "payload": {
    "version": {
      "application": "2018-10-03T12:45:50Z",
      "media": "2018-10-05T12:45:50Z"
    },
    "display": {
      "type": "1",
      "res": {
        "height": 360,
        "width": 1080
      }
    },
    "stats": {
      "logEntries": {
        "error": 0,
        "warning": 14,
        "info": 123
      },
      "lastLoaded": "2018-10-31T12:45:45Z",
      "pingFreq": 3600,
      "usedStorage": "124kb"
    }
  }
}
```

# DPIDiagnostics Properties

| Property                          | Type          | Required | Nullable       | Defined by                                                                                                               |
| :-------------------------------- | ------------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------- |
| [eventTimestamp](#eventtimestamp) | `string`      | Required | cannot be null | [DPIDiagnostics](dpi-diagnostics-properties-eventtimestamp.md "\#/properties/eventTimestamp#/properties/eventTimestamp") |
| [screenId](#screenid)             | `string`      | Required | cannot be null | [DPIDiagnostics](dpi-diagnostics-properties-screenid.md "\#/properties/screenId#/properties/screenId")                   |
| [type](#type)                     | `string`      | Required | cannot be null | [DPIDiagnostics](dpi-diagnostics-properties-type.md "\#/properties/type#/properties/type")                               |
| [payload](#payload)               | Not specified | Required | cannot be null | [DPIDiagnostics](dpi-diagnostics-properties-payload.md "\#/properties/payload#/properties/payload")                      |
| Additional Properties             | Any           | Optional | can be null    |                                                                                                                          |

## eventTimestamp

ISO 8601


`eventTimestamp`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [DPIDiagnostics](dpi-diagnostics-properties-eventtimestamp.md "\#/properties/eventTimestamp#/properties/eventTimestamp")

### eventTimestamp Type

`string`

## screenId




`screenId`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [DPIDiagnostics](dpi-diagnostics-properties-screenid.md "\#/properties/screenId#/properties/screenId")

### screenId Type

`string`

### screenId Examples

```json
"ad71dba8-c881-11e8-a8d5-f2801f1b9fd1"
```

## type

Diagnostics type


`type`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [DPIDiagnostics](dpi-diagnostics-properties-type.md "\#/properties/type#/properties/type")

### type Type

`string`

### type Examples

```json
"STATUS"
```

```json
"HEARTBEAT"
```

## payload

Diagnostics payload


`payload`

-   is required
-   Type: unknown
-   cannot be null
-   defined in: [DPIDiagnostics](dpi-diagnostics-properties-payload.md "\#/properties/payload#/properties/payload")

### payload Type

unknown

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
