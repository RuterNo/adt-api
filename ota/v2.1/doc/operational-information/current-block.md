# [v2.1](../../README.md) / [Operational information](README.md) / Current block 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/oi/current_block/state```  | ```true``` | ```1```

# CurrentBlock Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/current-block.json
```

Normally this topic indicates which block this vehicle is currently signed on to according to the backoffice or that it only assigned but not yet signed on or that it is not even assigned. This is usually a result of what was proposed by the driver on-board (see ruter/{PTO}/{vehicleID}/di/assignment_attempt/block) and then confirmed as valid by the back-office. It could also be based on an overriding decision enforced by the operation control centre.

Note that if a ruter/{PTO}/{vehicleID}/di/assignment_attempt/block is not answered by the back-office within a configured duration it is assumed that contact is lost with the control centre and then the proposed block will be accepted and exposed on this topic.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                           |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ---------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [current-block.json](../../schema/operational-information/current-block.json "open original schema") |

## CurrentBlock Type

`object` ([CurrentBlock](current-block.md))

## CurrentBlock Examples

```json
{
  "fromDateTime": "2017-10-31T12:45:50+01:00",
  "state": "SIGNED_ON",
  "blockRef": "10023",
  "operatingDay": "2017-10-31"
}
```

# CurrentBlock Properties

| Property                      | Type     | Required | Nullable       | Defined by                                                                                                     |
| :---------------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------- |
| [fromDateTime](#fromdatetime) | `string` | Required | cannot be null | [CurrentBlock](current-block-properties-fromdatetime.md "\#/properties/fromDateTime#/properties/fromDateTime") |
| [state](#state)               | `string` | Required | cannot be null | [CurrentBlock](current-block-properties-state.md "\#/properties/state#/properties/state")                      |
| [blockRef](#blockref)         | `string` | Optional | cannot be null | [CurrentBlock](current-block-properties-blockref.md "\#/properties/blockRef#/properties/blockRef")             |
| [operatingDay](#operatingday) | `string` | Optional | cannot be null | [CurrentBlock](current-block-properties-operatingday.md "\#/properties/operatingDay#/properties/operatingDay") |
| Additional Properties         | Any      | Optional | can be null    |                                                                                                                |

## fromDateTime

Time from which the sign on or assignment applies. ISO 8601, UTC.


`fromDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [CurrentBlock](current-block-properties-fromdatetime.md "\#/properties/fromDateTime#/properties/fromDateTime")

### fromDateTime Type

`string`

## state

Possible values in examples.


`state`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [CurrentBlock](current-block-properties-state.md "\#/properties/state#/properties/state")

### state Type

`string`

### state Examples

```json
"SIGNED_ON"
```

```json
"ASSIGNED"
```

```json
"NOT_ASSIGNED"
```

## blockRef

Not provided if not assigned or not signed on, otherwise provided as a Block identifier.


`blockRef`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [CurrentBlock](current-block-properties-blockref.md "\#/properties/blockRef#/properties/blockRef")

### blockRef Type

`string`

## operatingDay

Not provided if not assigned, otherwise provided as the scheduled date of the block on the format “YYYY-MM-DD”. Maybe different from calendar date.


`operatingDay`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [CurrentBlock](current-block-properties-operatingday.md "\#/properties/operatingDay#/properties/operatingDay")

### operatingDay Type

`string`

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
