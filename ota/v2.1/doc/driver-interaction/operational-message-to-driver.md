# [v2.1](../../README.md) / [Driver interaction](README.md) / Operational message to driver 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/di/operational_message_to_driver```  | ```false``` | ```1```

# OperationalMessageToDriver Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/driver-interaction/operational-message-to-driver.json
```

Provides an operational message directed to the driver onboard this vehicle. Direction: From back-office


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                      |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [operational-message-to-driver.json](../../schema/driver-interaction/operational-message-to-driver.json "open original schema") |

## OperationalMessageToDriver Type

`object` ([OperationalMessageToDriver](operational-message-to-driver.md))

## OperationalMessageToDriver Examples

```json
{
  "heading": "Emergency repair",
  "body": "Service personnel will meet at terminus to adjust door mechanism.",
  "senderRef": "Garage maintenance",
  "atDateTime": "2020-10-31T12:45:50Z"
}
```

# OperationalMessageToDriver Properties

| Property                  | Type     | Required | Nullable       | Defined by                                                                                                                             |
| :------------------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------- |
| [heading](#heading)       | `string` | Required | cannot be null | [OperationalMessageToDriver](operational-message-to-driver-properties-heading.md "\#/properties/heading#/properties/heading")          |
| [body](#body)             | `string` | Required | cannot be null | [OperationalMessageToDriver](operational-message-to-driver-properties-body.md "\#/properties/body#/properties/body")                   |
| [senderRef](#senderref)   | `string` | Required | cannot be null | [OperationalMessageToDriver](operational-message-to-driver-properties-senderref.md "\#/properties/senderRef#/properties/senderRef")    |
| [atDateTime](#atdatetime) | `string` | Required | cannot be null | [OperationalMessageToDriver](operational-message-to-driver-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime") |
| Additional Properties     | Any      | Optional | can be null    |                                                                                                                                        |

## heading




`heading`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [OperationalMessageToDriver](operational-message-to-driver-properties-heading.md "\#/properties/heading#/properties/heading")

### heading Type

`string`

## body




`body`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [OperationalMessageToDriver](operational-message-to-driver-properties-body.md "\#/properties/body#/properties/body")

### body Type

`string`

## senderRef




`senderRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [OperationalMessageToDriver](operational-message-to-driver-properties-senderref.md "\#/properties/senderRef#/properties/senderRef")

### senderRef Type

`string`

## atDateTime

ISO 8601


`atDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [OperationalMessageToDriver](operational-message-to-driver-properties-atdatetime.md "\#/properties/atDateTime#/properties/atDateTime")

### atDateTime Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
