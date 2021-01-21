# [v2.0](../../README.md) / [Operational information](README.md) / Unique identifier 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```oi/vehicle/unique_identifier```  | ```true``` | ```1```

# UniqueIdentifier Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/unique-identifier.json
```

A primary and permanent unique identifier used to represent the physical vehicle. For road vehicles: Indicates the globally unique 17 characters long alphanumeric Vehicle Identification Number (VIN) permanently attached to the vehicle. For other modes: Indicates a globally unique number of some sort permanently attached to the vehicle or if this is not possible; to the on-board system. Could be a MAC-address or other GUID.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                   |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [unique-identifier.json](../../schema/operational-information/unique-identifier.json "open original schema") |

## UniqueIdentifier Type

`object` ([UniqueIdentifier](unique-identifier.md))

## UniqueIdentifier Examples

```json
{
  "value": "1HGCM82633A004352",
  "typeOfValue": "VIN"
}
```

# UniqueIdentifier Properties

| Property                    | Type     | Required | Nullable       | Defined by                                                                                                          |
| :-------------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------ |
| [value](#value)             | `string` | Required | cannot be null | [UniqueIdentifier](unique-identifier-properties-value.md "\#/properties/value#/properties/value")                   |
| [typeOfValue](#typeofvalue) | `string` | Required | cannot be null | [UniqueIdentifier](unique-identifier-properties-typeofvalue.md "\#/properties/typeOfValue#/properties/typeOfValue") |
| Additional Properties       | Any      | Optional | can be null    |                                                                                                                     |

## value

Normally a 17 characters long alphanumeric Vehicle Identification Number (VIN) permanently attached to the vehicle by the vehicle manufacturer. For non-road vehicles where such a permanent identifier is not available or if the VIN is not known some other type of globally unique value could be used.


`value`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [UniqueIdentifier](unique-identifier-properties-value.md "\#/properties/value#/properties/value")

### value Type

`string`

## typeOfValue

Possible values in examples.


`typeOfValue`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [UniqueIdentifier](unique-identifier-properties-typeofvalue.md "\#/properties/typeOfValue#/properties/typeOfValue")

### typeOfValue Type

`string`

### typeOfValue Examples

```json
"VIN"
```

```json
"UUID"
```

```json
"PIN"
```

```json
"OTHER"
```

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
