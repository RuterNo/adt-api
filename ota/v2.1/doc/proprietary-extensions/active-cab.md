# [v2.1](../../README.md) / [Proprietary extensions](README.md) / Active cab 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```ruter/{PTO}/{vehicleID}/pe/activecab```  | ```true``` | ```1```

# ActiveCab Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/proprietary-extensions/active-cab.json
```

Used to keep track of what direction the train is driving

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                    |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :-------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [active-cab.json](../../schema/proprietary-extensions/active-cab.json "open original schema") |

## ActiveCab Type

`object` ([ActiveCab](active-cab.md))

## ActiveCab Examples

```json
{
  "eventTimestamp": "2020-10-31T08:38:02.749Z",
  "activeCab": "c1"
}
```

# ActiveCab Properties

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                    |
| :-------------------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------ |
| [eventTimestamp](#eventtimestamp) | `string` | Required | cannot be null | [ActiveCab](active-cab-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp") |
| [activeCab](#activecab)           | `string` | Required | cannot be null | [ActiveCab](active-cab-properties-activecab.md "#/properties/activeCab#/properties/activeCab")                |
| Additional Properties             | Any      | Optional | can be null    |                                                                                                               |

## eventTimestamp

ISO 8601, UTC

`eventTimestamp`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ActiveCab](active-cab-properties-eventtimestamp.md "#/properties/eventTimestamp#/properties/eventTimestamp")

### eventTimestamp Type

`string`

## activeCab

Text for active cab

`activeCab`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ActiveCab](active-cab-properties-activecab.md "#/properties/activeCab#/properties/activeCab")

### activeCab Type

`string`

### activeCab Examples

```json
"c1"
```

```json
"c2"
```

```json
"inactive"
```

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
