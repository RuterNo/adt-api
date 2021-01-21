# [v2.0](../../README.md) / [Proprietary extensions](README.md) / Dpi acknowledge 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/pe/dpi_ack```  | ```false``` | ```1```

# DPIAcknowledge Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/proprietary-extensions/dpi-acknowledge.json
```

The DPI Ack topic is used to inform the Ruter BO about the content presented on the PTO’s own systems for Dynamic Passenger Information in the vehicle. Usually, this is destination displays. The rest of DPI is presented by Ruter’s own DPI system, and does not need this kind of acknowledgement message.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                              |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [dpi-acknowledge.json](../../schema/proprietary-extensions/dpi-acknowledge.json "open original schema") |

## DPIAcknowledge Type

`object` ([DPIAcknowledge](dpi-acknowledge.md))

## DPIAcknowledge Examples

```json
{
  "eventTimestamp": "2021-10-31T12:45:50Z",
  "type": "DESTINATION",
  "payload": {
    "text": "400 Oslo Lufthavn",
    "additionalText": "o/ Eltonåsen"
  }
}
```

# DPIAcknowledge Properties

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                               |
| :-------------------------------- | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------- |
| [eventTimestamp](#eventtimestamp) | `string` | Required | cannot be null | [DPIAcknowledge](dpi-acknowledge-properties-eventtimestamp.md "\#/properties/eventTimestamp#/properties/eventTimestamp") |
| [type](#type)                     | `string` | Required | cannot be null | [DPIAcknowledge](dpi-acknowledge-properties-type.md "\#/properties/type#/properties/type")                               |
| [payload](#payload)               | `object` | Required | cannot be null | [DPIAcknowledge](dpi-acknowledge-properties-payload.md "\#/properties/payload#/properties/payload")                      |
| Additional Properties             | Any      | Optional | can be null    |                                                                                                                          |

## eventTimestamp

ISO 8601


`eventTimestamp`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [DPIAcknowledge](dpi-acknowledge-properties-eventtimestamp.md "\#/properties/eventTimestamp#/properties/eventTimestamp")

### eventTimestamp Type

`string`

## type




`type`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [DPIAcknowledge](dpi-acknowledge-properties-type.md "\#/properties/type#/properties/type")

### type Type

`string`

### type Examples

```json
"AUDIO"
```

```json
"DESTINATION"
```

## payload

Destination text strings.


`payload`

-   is required
-   Type: `object` ([Details](dpi-acknowledge-properties-payload.md))
-   cannot be null
-   defined in: [DPIAcknowledge](dpi-acknowledge-properties-payload.md "\#/properties/payload#/properties/payload")

### payload Type

`object` ([Details](dpi-acknowledge-properties-payload.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
