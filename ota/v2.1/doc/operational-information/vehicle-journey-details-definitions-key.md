# Key Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/key
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## key Type

`object` ([Key](vehicle-journey-details-definitions-key.md))

# key Properties

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                              |
| :------------------------------ | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [deviceName](#devicename)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-devicename.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/key/properties/deviceName")       |
| [typeCode](#typecode)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-typecode.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/key/properties/typeCode")           |
| [parameterData](#parameterdata) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-parameterdata.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/key/properties/parameterData") |

## deviceName

Name of devices for which this key applies.

`deviceName`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-devicename.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/key/properties/deviceName")

### deviceName Type

`string`

## typeCode

Name of data type.

`typeCode`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-typecode.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/key/properties/typeCode")

### typeCode Type

`string`

## parameterData

The data formatted in an agreed (that could be customer specific) format for the specified DeviceName and TypeCode.

`parameterData`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-parameterdata.md "https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/key/properties/parameterData")

### parameterData Type

`string`
