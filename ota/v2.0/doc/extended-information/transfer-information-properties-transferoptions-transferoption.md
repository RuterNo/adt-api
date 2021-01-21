# transferOption Schema

```txt
#/properties/transferOptions#/properties/transferOptions/items
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                        |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [transfer-information.json\*](../../schema/extended-information/transfer-information.json "open original schema") |

## items Type

`object` ([transferOption](transfer-information-properties-transferoptions-transferoption.md))

# transferOption Properties

| Property                                            | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                       |
| :-------------------------------------------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [transportMode](#transportmode)                     | `string` | Required | cannot be null | [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-transportmode.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/transportMode")                     |
| [lineDesignation](#linedesignation)                 | `string` | Required | cannot be null | [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-linedesignation.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/lineDesignation")                 |
| [destinationDisplayName](#destinationdisplayname)   | `string` | Required | cannot be null | [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-destinationdisplayname.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/destinationDisplayName")   |
| [directionOfLineName](#directionoflinename)         | `string` | Optional | cannot be null | [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-directionoflinename.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/directionOfLineName")         |
| [stopPointDesignation](#stoppointdesignation)       | `string` | Optional | cannot be null | [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-stoppointdesignation.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/stopPointDesignation")       |
| [presentedDepartureTimes](#presenteddeparturetimes) | `array`  | Required | cannot be null | [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-presenteddeparturetimes.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/presentedDepartureTimes") |

## transportMode

Mode of transport.


`transportMode`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-transportmode.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/transportMode")

### transportMode Type

`string`

### transportMode Examples

```json
"BUS"
```

```json
"TRAIN"
```

```json
"FERRY"
```

```json
"METRO"
```

## lineDesignation

The line designation to display. This is often a number but can also be alphanumeric. Normally 1- 4 characters.


`lineDesignation`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-linedesignation.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/lineDesignation")

### lineDesignation Type

`string`

## destinationDisplayName

The name of the destination of the vehicle. This can be of any length but practically seldom over 30 characters.


`destinationDisplayName`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-destinationdisplayname.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/destinationDisplayName")

### destinationDisplayName Type

`string`

## directionOfLineName

Optional. The text denoting the direction of the vehicle. This can be of any length but practically seldom over 30 characters.


`directionOfLineName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-directionoflinename.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/directionOfLineName")

### directionOfLineName Type

`string`

### directionOfLineName Examples

```json
"Towards City Centre"
```

## stopPointDesignation

Optional. The designation of the stop from where departure will occur. Typically, a single or double letter or a digit that distinguish this stop point from other stop points within the stop area.


`stopPointDesignation`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-stoppointdesignation.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/stopPointDesignation")

### stopPointDesignation Type

`string`

## presentedDepartureTimes




`presentedDepartureTimes`

-   is required
-   Type: `string[]` ([presentedDepartureTimes](transfer-information-properties-transferoptions-transferoption-properties-presenteddeparturetimes-presenteddeparturetimes.md))
-   cannot be null
-   defined in: [TransferInformation](transfer-information-properties-transferoptions-transferoption-properties-presenteddeparturetimes.md "\#/properties/transferOptions#/properties/transferOptions/items/properties/presentedDepartureTimes")

### presentedDepartureTimes Type

`string[]` ([presentedDepartureTimes](transfer-information-properties-transferoptions-transferoption-properties-presenteddeparturetimes-presenteddeparturetimes.md))
