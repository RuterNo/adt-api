# [v2.1](../../README.md) / [Proprietary extensions](README.md) / Dpi command 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/pe/dpi_command```  | ```false``` | ```1```

# DPICommand Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/proprietary-extensions/dpi-command.json
```

The c2 channels are reserved for command and control messages originated by Ruter. Typical use cases include: • Diagnostics / debugging o Trigger transfer of debug information o Trigger screenshot of DPI screen o Trigger clearing of cache and refresh of webpage • Content of Trigger display of campaign The payload is defined as an object with no structure to provide flexibility.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                      |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [dpi-command.json](../../schema/proprietary-extensions/dpi-command.json "open original schema") |

## DPICommand Type

`object` ([DPICommand](dpi-command.md))

## DPICommand Examples

```json
{
  "eventTimestamp": "2018-10-31T12:45:50Z",
  "type": "DEBUG",
  "payload": {
    "command": "LOG_TRANSFER",
    "arg": {
      "level": "ERROR",
      "limit": 10,
      "page": 0
    }
  }
}
```

# DPICommand Properties

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                      |
| :-------------------------------- | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------- |
| [eventTimestamp](#eventtimestamp) | `string` | Required | cannot be null | [DPICommand](dpi-command-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp") |
| [type](#type)                     | `string` | Required | cannot be null | [DPICommand](dpi-command-properties-type.md "#/properties/type#/properties/type")                               |
| [payload](#payload)               | `object` | Required | cannot be null | [DPICommand](dpi-command-properties-payload.md "#/properties/payload#/properties/payload")                      |
| Additional Properties             | Any      | Optional | can be null    |                                                                                                                 |

## eventTimestamp

ISO 8601

`eventTimestamp`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DPICommand](dpi-command-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp")

### eventTimestamp Type

`string`

## type



`type`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DPICommand](dpi-command-properties-type.md "#/properties/type#/properties/type")

### type Type

`string`

## payload



`payload`

*   is required

*   Type: `object` ([Details](dpi-command-properties-payload.md))

*   cannot be null

*   defined in: [DPICommand](dpi-command-properties-payload.md "#/properties/payload#/properties/payload")

### payload Type

`object` ([Details](dpi-command-properties-payload.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
