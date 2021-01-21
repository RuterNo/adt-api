# [v2.0](../../README.md) / [Operational information](README.md) / Vehicle journey details 
 
MQTT topic                                          | Retain   | QoS 
| :------------------------------------------------ | -------- | -------- |
```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/details```  | ```true``` | ```1```

# VehicleJourneyDetails Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json
```

This topic provides the details of the current (monitored) vehicle journey. If there is no ongoing vehicle journey, this topic will provide the details of the coming vehicle journey. The information should reflect the latest production plan including any applied control actions as known in the back-office. Note however that this does not include neither estimated nor observed times at the different stops. This information is instead provided on the topic ruter/{PTO}/{vehicleID}/oi/current_vehicle_journey/expected_call The topic should be blanked (provided as a retained message with a zero-byte payload) if the vehicle has left the last stop and the next vehicle journey is not known.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                               |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| Can be instantiated | Yes        | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## VehicleJourneyDetails Type

`object` ([VehicleJourneyDetails](vehicle-journey-details.md))

## VehicleJourneyDetails Examples

```json
{
  "operatingDayDate": "2017-04-27T00:00:00+02:00",
  "vehicleJourneyRef": "9015001095045020",
  "journeyNumber": "45020",
  "journeyPatternRef": "4010000482522803",
  "timedJourneyPatternRef": "4010000482522978",
  "transportModeCode": "BUS",
  "line": {
    "ref": "9011001095000000",
    "designation": "22",
    "number": "950",
    "name": "Ersätter Tvärbanan"
  },
  "directionOfLine": {
    "code": "1",
    "name": "Solna"
  },
  "transportAuthority": {
    "ref": "9010001000000000",
    "code": "SL",
    "name": "Storstockholms Lokaltrafik",
    "number": "1"
  },
  "contractor": {
    "ref": "9013001001500000",
    "code": "ARR",
    "name": "Arriva",
    "number": "15"
  },
  "plannedStartDateTime": "2017-04-27T05:51:00+02:00",
  "plannedEndDateTime": "2017-04-27T06:39:00+02:00",
  "origin": {
    "name": "Sickla udde",
    "shortName": "Sickla udde"
  },
  "calls": [
    {
      "sequenceNumber": 1,
      "journeyPatternPoint": {
        "ref": "9025001000010664",
        "isTimingPoint": true,
        "location": {
          "latitude": 59.3071932996622,
          "longitude": 18.1078200699196
        },
        "distanceFromPrevious": 0,
        "detection": {
          "enteringDistance": 20,
          "exitingDistance": 10,
          "passingDirection": null
        }
      },
      "stopArea": {
        "ref": "9021001010665000",
        "name": "Sickla udde",
        "shortName": "Sickla udde"
      },
      "stopPoint": {
        "ref": "9022001010665005",
        "name": "Sickla udde",
        "shortName": "Sickla udde",
        "designation": "",
        "localNumber": 5,
        "length": 20
      },
      "arrival": {
        "latestDateTime": "2017-04-27T05:51:00+02:00",
        "arrivalType": "STOP_NO_ALIGHTING"
      },
      "departure": {
        "earliestDateTime": "2017-04-27T05:51:00+02:00",
        "departureType": "STOP_IF_BOARDING"
      },
      "destinationDisplay": {
        "productName": "",
        "symbolName": "",
        "lineDesignation": "22B",
        "primaryDestination": "Thorildsplan",
        "secondaryDestination": "Eriksbo värdshuset",
        "displayKeys": [
          {
            "parameterData": "Destination=653",
            "typeCode": "O_DESTIN",
            "deviceName": "SIGN"
          }
        ]
      }
    },
    {
      "sequenceNumber": 2,
      "journeyPatternPoint": {
        "ref": "9025001000010667",
        "isTimingPoint": true,
        "location": {
          "latitude": 59.97882,
          "longitude": 18.21584
        },
        "distanceFromPrevious": 652,
        "detection": {
          "enteringDistance": 20,
          "exitingDistance": 10,
          "passingDirection": null
        },
        "pathFromPrevious": {
          "coordinates": [
            [
              59.94525,
              18.13365
            ],
            [
              59.94562,
              18.17644
            ],
            [
              59.95361,
              18.18034
            ],
            [
              59.96939,
              18.19872
            ],
            [
              59.97882,
              18.21584
            ]
          ]
        }
      },
      "stopArea": {
        "ref": "9021001010667000",
        "name": "Eriksbo",
        "shortName": "Eriksbo"
      },
      "stopPoint": {
        "ref": "9022001010667001",
        "name": "Eriksbo",
        "shortName": "Eriksbo",
        "designation": "",
        "localNumber": 1,
        "length": 22,
        "stopPointKeys": [
          {
            "parameterData": "Värdshuset",
            "typeCode": "ADDITIONAL_INFO",
            "deviceName": "Alias"
          }
        ]
      },
      "replacedJourneyPatternPoint": {
        "ref": "9025001000010688",
        "isTimingPoint": true,
        "location": {
          "latitude": 59.94525,
          "longitude": 18.13365
        },
        "distanceFromPrevious": 555,
        "detection": {
          "enteringDistance": 20,
          "exitingDistance": 10,
          "passingDirection": null
        }
      },
      "replacedStopArea": {
        "ref": "9021001010995000",
        "name": "Sickla väg",
        "shortName": "Sickla väg"
      },
      "replacedStopPoint": {
        "ref": "9022001010995004",
        "name": "Sickla väg",
        "shortName": "Sickla väg",
        "designation": "",
        "localNumber": 4,
        "length": 20
      },
      "detourEnroute": {
        "startsAfterCallSequenceNumber": 1,
        "path": {
          "coordinates": [
            [
              59.94525,
              18.13365
            ],
            [
              59.94352,
              18.14644
            ],
            [
              59.95261,
              18.14034
            ],
            [
              59.96439,
              18.16872
            ],
            [
              59.97882,
              18.21584
            ]
          ]
        }
      },
      "arrival": {
        "latestDateTime": "2017-04-27T05:53:00+02:00",
        "arrivalType": "STOP_IF_ALIGHTING"
      },
      "departure": {
        "earliestDateTime": "2017-04-27T05:53:00+02:00",
        "departureType": "STOP_IF_BOARDING"
      },
      "destinationDisplay": {
        "productName": "",
        "symbolName": "",
        "lineDesignation": "22B",
        "primaryDestination": "Thorildsplan",
        "displayKeys": [
          {
            "parameterData": "Destination=659",
            "typeCode": "O_DESTIN",
            "deviceName": "SIGN"
          }
        ]
      },
      "fetcherConnections": [
        {
          "connectionRef": "9014001002310000",
          "transportModeCode": "BUS",
          "lineAuthorityCode": "SL",
          "lineDesignation": "23",
          "directionName": "Mot Hötorget",
          "minChangeDurationSeconds": 120,
          "maxWaitingUntilTime": "2017-04-27T06:05:00+02:00"
        },
        {
          "connectionRef": "9014001002410000",
          "transportModeCode": "BUS",
          "lineAuthorityCode": "SL",
          "lineDesignation": "24",
          "directionName": "Mot Rådhuset",
          "minChangeDurationSeconds": 60,
          "maxWaitingUntilTime": "2017-04-27T06:03:00+02:00"
        }
      ]
    }
  ]
}
```

# VehicleJourneyDetails Properties

| Property                                          | Type     | Required | Nullable       | Defined by                                                                                                                                                      |
| :------------------------------------------------ | -------- | -------- | -------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [operatingDayDate](#operatingdaydate)             | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-operatingdaydate.md "\#/properties/operatingDayDate#/properties/operatingDayDate")                   |
| [vehicleJourneyRef](#vehiclejourneyref)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-vehiclejourneyref.md "\#/properties/vehicleJourneyRef#/properties/vehicleJourneyRef")                |
| [journeyNumber](#journeynumber)                   | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-journeynumber.md "\#/properties/journeyNumber#/properties/journeyNumber")                            |
| [journeyPatternRef](#journeypatternref)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-journeypatternref.md "\#/properties/journeyPatternRef#/properties/journeyPatternRef")                |
| [timedJourneyPatternRef](#timedjourneypatternref) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-timedjourneypatternref.md "\#/properties/timedJourneyPatternRef#/properties/timedJourneyPatternRef") |
| [transportModeCode](#transportmodecode)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-transportmodecode.md "\#/properties/transportModeCode#/properties/transportModeCode")                |
| [transportAuthority](#transportauthority)         | `object` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-organisation-info.md "\#/properties/transportAuthority#/properties/transportAuthority")              |
| [contractor](#contractor)                         | `object` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-organisation-info-1.md "\#/properties/contractor#/properties/contractor")                            |
| [plannedStartDateTime](#plannedstartdatetime)     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-plannedstartdatetime.md "\#/properties/plannedStartDateTime#/properties/plannedStartDateTime")       |
| [plannedEndDateTime](#plannedenddatetime)         | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-plannedenddatetime.md "\#/properties/plannedEndDateTime#/properties/plannedEndDateTime")             |
| [origin](#origin)                                 | `object` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-place.md "\#/properties/origin#/properties/origin")                                                  |
| [line](#line)                                     | `object` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-line-info.md "\#/properties/line#/properties/line")                                                  |
| [directionOfLine](#directionofline)               | `object` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-direction-of-line-info.md "\#/properties/directionOfLine#/properties/directionOfLine")               |
| [calls](#calls)                                   | `array`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-properties-calls.md "\#/properties/calls#/properties/calls")                                                    |
| Additional Properties                             | Any      | Optional | can be null    |                                                                                                                                                                 |

## operatingDayDate

The scheduled date of the journey.


`operatingDayDate`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-operatingdaydate.md "\#/properties/operatingDayDate#/properties/operatingDayDate")

### operatingDayDate Type

`string`

## vehicleJourneyRef

A Vehicle Journey identifier.


`vehicleJourneyRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-vehiclejourneyref.md "\#/properties/vehicleJourneyRef#/properties/vehicleJourneyRef")

### vehicleJourneyRef Type

`string`

## journeyNumber

The journey number. May describe a part of the vehicleJourneyRef that should be interpreted in scope of a certain line or an operator.


`journeyNumber`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-journeynumber.md "\#/properties/journeyNumber#/properties/journeyNumber")

### journeyNumber Type

`string`

## journeyPatternRef

A unique identifier for the original journey pattern. E.g. 16-digit ID.


`journeyPatternRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-journeypatternref.md "\#/properties/journeyPatternRef#/properties/journeyPatternRef")

### journeyPatternRef Type

`string`

## timedJourneyPatternRef

Optional. Identifier for a journey pattern with a unique timing pattern. Format to be agreed.


`timedJourneyPatternRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-timedjourneypatternref.md "\#/properties/timedJourneyPatternRef#/properties/timedJourneyPatternRef")

### timedJourneyPatternRef Type

`string`

## transportModeCode

The transport mode.


`transportModeCode`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-transportmodecode.md "\#/properties/transportModeCode#/properties/transportModeCode")

### transportModeCode Type

`string`

### transportModeCode Examples

```json
"BUS"
```

```json
"TRAM"
```

## transportAuthority

Information about the transport authority that provides the journey.


`transportAuthority`

-   is required
-   Type: `object` ([Organisation Info](vehicle-journey-details-properties-organisation-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-organisation-info.md "\#/properties/transportAuthority#/properties/transportAuthority")

### transportAuthority Type

`object` ([Organisation Info](vehicle-journey-details-properties-organisation-info.md))

## contractor

Optional. Information about the operator that is contracted to operate the journey.


`contractor`

-   is optional
-   Type: `object` ([Organisation Info](vehicle-journey-details-properties-organisation-info-1.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-organisation-info-1.md "\#/properties/contractor#/properties/contractor")

### contractor Type

`object` ([Organisation Info](vehicle-journey-details-properties-organisation-info-1.md))

## plannedStartDateTime

The date and time when the journey is planned to start. ISO 8601, UTC.


`plannedStartDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-plannedstartdatetime.md "\#/properties/plannedStartDateTime#/properties/plannedStartDateTime")

### plannedStartDateTime Type

`string`

## plannedEndDateTime

The date and time when the journey is planned to end. ISO 8601, UTC.


`plannedEndDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-plannedenddatetime.md "\#/properties/plannedEndDateTime#/properties/plannedEndDateTime")

### plannedEndDateTime Type

`string`

## origin

The place where the journey comes from.


`origin`

-   is required
-   Type: `object` ([Place](vehicle-journey-details-properties-place.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-place.md "\#/properties/origin#/properties/origin")

### origin Type

`object` ([Place](vehicle-journey-details-properties-place.md))

## line

Optional. Only provided for service journeys. Information about the journey’s line.


`line`

-   is optional
-   Type: `object` ([Line Info](vehicle-journey-details-properties-line-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-line-info.md "\#/properties/line#/properties/line")

### line Type

`object` ([Line Info](vehicle-journey-details-properties-line-info.md))

## directionOfLine

Optional. Only provided for service journeys. Information about the journey’s direction on the line.


`directionOfLine`

-   is optional
-   Type: `object` ([Direction Of Line Info](vehicle-journey-details-properties-direction-of-line-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-direction-of-line-info.md "\#/properties/directionOfLine#/properties/directionOfLine")

### directionOfLine Type

`object` ([Direction Of Line Info](vehicle-journey-details-properties-direction-of-line-info.md))

## calls

Points that shall be called at during the journey. At least two items.


`calls`

-   is required
-   Type: unknown\[]
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-properties-calls.md "\#/properties/calls#/properties/calls")

### calls Type

unknown\[]

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema

# VehicleJourneyDetails Definitions

## Definitions group lineInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo"}
```

| Property                    | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                          |
| :-------------------------- | -------- | -------- | -------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref)                 | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/ref")                 |
| [designation](#designation) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/designation") |
| [number](#number)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/number")           |
| [name](#name)               | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/name")               |

### ref

Optional. Only provided for service journeys. Information about the journey’s line.


`ref`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/ref")

#### ref Type

`string`

### designation

The public line number displayed to passengers. Note: this value can be alphanumeric!


`designation`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/designation")

#### designation Type

`string`

### number

Technical line number.


`number`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/number")

#### number Type

`string`

### name

Optional. Name of line.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/lineInfo/properties/name")

#### name Type

`string`

## Definitions group directionOfLineInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo"}
```

| Property        | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                    |
| :-------------- | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [code](#code)   | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/code") |
| [name](#name-1) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/name") |

### code

A value that is unique per direction.


`code`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/code")

#### code Type

`string`

#### code Examples

```json
"1"
```

```json
"2"
```

### name

Optional. Name of direction.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-direction-of-line-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/directionOfLineInfo/properties/name")

#### name Type

`string`

## Definitions group place

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place"}
```

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                               |
| :---------------------- | -------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name-2)         | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/name")           |
| [shortName](#shortname) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/shortName") |

### name

Optional. Name of the origin.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/name")

#### name Type

`string`

### shortName

Optional. Short name of the origin.


`shortName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-place-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/place/properties/shortName")

#### shortName Type

`string`

## Definitions group destinationDisplay

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay"}
```

| Property                                      | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                |
| :-------------------------------------------- | -------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [productName](#productname)                   | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-productname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/productName")                   |
| [symbolName](#symbolname)                     | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-symbolname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/symbolName")                     |
| [lineDesignation](#linedesignation)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-linedesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/lineDesignation")           |
| [primaryDestination](#primarydestination)     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-primarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/primaryDestination")     |
| [secondaryDestination](#secondarydestination) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-secondarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/secondaryDestination") |
| [displayKeys](#displaykeys)                   | `array`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-displaykeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/displayKeys")                   |

### productName

Optional. Name of public transport product.


`productName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-productname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/productName")

#### productName Type

`string`

### symbolName

Optional. Controls any symbols in display.


`symbolName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-symbolname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/symbolName")

#### symbolName Type

`string`

### lineDesignation

Displayed line number.


`lineDesignation`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-linedesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/lineDesignation")

#### lineDesignation Type

`string`

### primaryDestination

Names of primary destination.


`primaryDestination`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-primarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/primaryDestination")

#### primaryDestination Type

`string`

### secondaryDestination

Optional. Names of secondary destination.


`secondaryDestination`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-secondarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/secondaryDestination")

#### secondaryDestination Type

`string`

### displayKeys

Optional. Contains device specific information such as sign codes etcetera. See 5.6.20. A numeric sign code representing the combined destination display information could thus be provided in a contained key with appropriate parameterData. E.g. “Destination=659” It is possible to provide information for multiple display devices in parallel if there is a mixed fleet with different hardware by providing multiple Keys in parallel. E.g. one Key with "deviceName": "SIGN_X" and another Key with "deviceName": "SIGN_Y".


`displayKeys`

-   is optional
-   Type: `object[]` ([Key](vehicle-journey-details-definitions-destination-display-properties-displaykeys-key.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-displaykeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/displayKeys")

#### displayKeys Type

`object[]` ([Key](vehicle-journey-details-definitions-destination-display-properties-displaykeys-key.md))

## Definitions group primaryDestination

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/primaryDestination"}
```

| Property                  | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                          |
| :------------------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [name](#name-3)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/name")           |
| [shortName](#shortname-1) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/shortName") |

### name

Name of the destination.


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/name")

#### name Type

`string`

### shortName

Optional. Short name of the destination.


`shortName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-primary-destination-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/primaryDestination/properties/shortName")

#### shortName Type

`string`

## Definitions group secondaryDestination

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination"}
```

| Property                                              | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                            |
| :---------------------------------------------------- | -------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name-4)                                       | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/name")                                         |
| [shortName](#shortname-2)                             | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/shortName")                               |
| [secondaryDestinationType](#secondarydestinationtype) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-secondarydestinationtype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/secondaryDestinationType") |

### name

Optional. Name of the destination.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/name")

#### name Type

`string`

### shortName

Optional. Short name of the destination.


`shortName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/shortName")

#### shortName Type

`string`

### secondaryDestinationType

Optional. The meaning of the secondary destination.


`secondaryDestinationType`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-secondary-destination-properties-secondarydestinationtype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/secondaryDestination/properties/secondaryDestinationType")

#### secondaryDestinationType Type

`string`

## Definitions group pointCall

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall"}
```

| Property                                                    | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                             |
| :---------------------------------------------------------- | --------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sequenceNumber](#sequencenumber)                           | `number`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-sequencenumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/sequenceNumber")                            |
| [journeyPatternPoint](#journeypatternpoint)                 | `object`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/journeyPatternPoint")           |
| [stopArea](#stoparea)                                       | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-area-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopArea")                                  |
| [stopPoint](#stoppoint)                                     | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopPoint")                                |
| [arrival](#arrival)                                         | `object`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-arrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/arrival")                                          |
| [departure](#departure)                                     | `object`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-departure.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/departure")                                      |
| [destinationDisplay](#destinationdisplay)                   | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/destinationDisplay")                                         |
| [isCancelledCall](#iscancelledcall)                         | `boolean` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-iscancelledcall.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/isCancelledCall")                          |
| [replacedJourneyPatternPoint](#replacedjourneypatternpoint) | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info-1.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedJourneyPatternPoint") |
| [replacedStopArea](#replacedstoparea)                       | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-area-info-1.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopArea")                        |
| [replacedStopPoint](#replacedstoppoint)                     | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-point-info-1.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopPoint")                      |
| [FetcherConnections](#fetcherconnections)                   | `array`   | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-fetcherconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/FetcherConnections")                    |
| [FeederConnections](#feederconnections)                     | `array`   | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-feederconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/FeederConnections")                      |

### sequenceNumber

The order of the call on the vehicle journey. Increasing. Note that the numbering can start with a higher number than 1 and that there might be holes in the sequence numbering as not expected calls are excluded.


`sequenceNumber`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-sequencenumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/sequenceNumber")

#### sequenceNumber Type

`number`

### journeyPatternPoint

The point to call. (May be updated in real time).


`journeyPatternPoint`

-   is required
-   Type: `object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/journeyPatternPoint")

#### journeyPatternPoint Type

`object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info.md))

### stopArea

Optional. The stop area of the call. (May be updated in real time).


`stopArea`

-   is optional
-   Type: `object` ([Stop Area Info](vehicle-journey-details-definitions-point-call-properties-stop-area-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-area-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopArea")

#### stopArea Type

`object` ([Stop Area Info](vehicle-journey-details-definitions-point-call-properties-stop-area-info.md))

### stopPoint

Optional. The stop point of the call. (May be updated in real time).


`stopPoint`

-   is optional
-   Type: `object` ([Stop Point Info](vehicle-journey-details-definitions-point-call-properties-stop-point-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-point-info.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/stopPoint")

#### stopPoint Type

`object` ([Stop Point Info](vehicle-journey-details-definitions-point-call-properties-stop-point-info.md))

### arrival




`arrival`

-   is required
-   Type: `object` ([Arrival](vehicle-journey-details-definitions-point-call-properties-arrival.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-arrival.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/arrival")

#### arrival Type

`object` ([Arrival](vehicle-journey-details-definitions-point-call-properties-arrival.md))

### departure




`departure`

-   is required
-   Type: `object` ([Departure](vehicle-journey-details-definitions-point-call-properties-departure.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-departure.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/departure")

#### departure Type

`object` ([Departure](vehicle-journey-details-definitions-point-call-properties-departure.md))

### destinationDisplay

Optional.


`destinationDisplay`

-   is optional
-   Type: `object` ([Destination Display](vehicle-journey-details-definitions-destination-display.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/destinationDisplay")

#### destinationDisplay Type

`object` ([Destination Display](vehicle-journey-details-definitions-destination-display.md))

### isCancelledCall

Optional. Only provided if true. Boolean that indicates if this is call is cancelled without being replaced. In this case the call to the above-mentioned stop should be presented as cancelled.


`isCancelledCall`

-   is optional
-   Type: `boolean`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-iscancelledcall.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/isCancelledCall")

#### isCancelledCall Type

`boolean`

#### isCancelledCall Examples

```json
"true"
```

```json
"false"
```

### replacedJourneyPatternPoint

Optional. Only provided if the original Journey Pattern Point is replaced. Describes the replaced point. Represents the original (planned) information.


`replacedJourneyPatternPoint`

-   is optional
-   Type: `object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info-1.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info-1.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedJourneyPatternPoint")

#### replacedJourneyPatternPoint Type

`object` ([Journey Pattern Point Info](vehicle-journey-details-definitions-point-call-properties-journey-pattern-point-info-1.md))

### replacedStopArea

Optional. Only present if the original StopArea is replaced. Describes the replaced stop area. Represents the original (planned) information.


`replacedStopArea`

-   is optional
-   Type: `object` ([Stop Area Info](vehicle-journey-details-definitions-point-call-properties-stop-area-info-1.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-area-info-1.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopArea")

#### replacedStopArea Type

`object` ([Stop Area Info](vehicle-journey-details-definitions-point-call-properties-stop-area-info-1.md))

### replacedStopPoint

Optional. Only present if the original StopPoint is replaced. Describes the replaced stop point. Represents the original (planned) information.


`replacedStopPoint`

-   is optional
-   Type: `object` ([Stop Point Info](vehicle-journey-details-definitions-point-call-properties-stop-point-info-1.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-stop-point-info-1.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/replacedStopPoint")

#### replacedStopPoint Type

`object` ([Stop Point Info](vehicle-journey-details-definitions-point-call-properties-stop-point-info-1.md))

### FetcherConnections

Optional. Planned fetcher (distributor) protected connections. A list of vehicle journeys that must wait for passengers from this vehicle journey at this stop even if it is delayed. Relevant for passenger information.


`FetcherConnections`

-   is optional
-   Type: `object[]` ([Connection Info](vehicle-journey-details-definitions-point-call-properties-fetcherconnections-connection-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-fetcherconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/FetcherConnections")

#### FetcherConnections Type

`object[]` ([Connection Info](vehicle-journey-details-definitions-point-call-properties-fetcherconnections-connection-info.md))

### FeederConnections

Optional. Planned feeder protected connections. A list of vehicle journeys that this vehicle journey should await passengers from at this stop even if the feeding journeys are delayed. Relevant for driver information.


`FeederConnections`

-   is optional
-   Type: `object[]` ([Connection Info](vehicle-journey-details-definitions-point-call-properties-feederconnections-connection-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-point-call-properties-feederconnections.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/FeederConnections")

#### FeederConnections Type

`object[]` ([Connection Info](vehicle-journey-details-definitions-point-call-properties-feederconnections-connection-info.md))

## Definitions group journeyPatternPointInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo"}
```

| Property                                      | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                            |
| :-------------------------------------------- | --------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref-1)                                 | `string`  | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/ref")                                   |
| [isTimingPoint](#istimingpoint)               | `boolean` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-istimingpoint.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/isTimingPoint")               |
| [location](#location)                         | `object`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-position.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/location")                         |
| [distanceFromPrevious](#distancefromprevious) | `number`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-distancefromprevious.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/distanceFromPrevious") |
| [tariffZones](#tariffzones)                   | `array`   | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-tariffzones.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/tariffZones")                   |

### ref

Id of journey pattern point.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/ref")

#### ref Type

`string`

### isTimingPoint

Boolean that indicates if this is a point where the driver should respect the departure time.


`isTimingPoint`

-   is required
-   Type: `boolean`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-istimingpoint.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/isTimingPoint")

#### isTimingPoint Type

`boolean`

#### isTimingPoint Examples

```json
"true"
```

```json
"false"
```

### location

Optional. The position of the point in Latitude/Longitude.


`location`

-   is optional
-   Type: `object` ([Position](vehicle-journey-details-definitions-journey-pattern-point-info-properties-position.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-position.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/location")

#### location Type

`object` ([Position](vehicle-journey-details-definitions-journey-pattern-point-info-properties-position.md))

### distanceFromPrevious

Optional. Meters from previous point. The first call has the value zero.


`distanceFromPrevious`

-   is optional
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-distancefromprevious.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/distanceFromPrevious")

#### distanceFromPrevious Type

`number`

### tariffZones

Optional. Tariff Zones valid for this point.


`tariffZones`

-   is optional
-   Type: `object[]` ([Tariff Zone Info](vehicle-journey-details-definitions-journey-pattern-point-info-properties-tariffzones-tariff-zone-info.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-journey-pattern-point-info-properties-tariffzones.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/journeyPatternPointInfo/properties/tariffZones")

#### tariffZones Type

`object[]` ([Tariff Zone Info](vehicle-journey-details-definitions-journey-pattern-point-info-properties-tariffzones-tariff-zone-info.md))

## Definitions group position

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/position"}
```

| Property                | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                     |
| :---------------------- | -------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [latitude](#latitude)   | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-latitude.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/position/properties/latitude")   |
| [longitude](#longitude) | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-longitude.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/position/properties/longitude") |

### latitude

The latitude in decimal degrees.


`latitude`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-latitude.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/position/properties/latitude")

#### latitude Type

`number`

### longitude

The longitude in decimal degrees.


`longitude`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-position-properties-longitude.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/position/properties/longitude")

#### longitude Type

`number`

## Definitions group stopAreaInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo"}
```

| Property                  | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                               |
| :------------------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref-2)             | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/ref")             |
| [name](#name-5)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/name")           |
| [shortName](#shortname-3) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/shortName") |

### ref

Id of the Stop Area.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/ref")

#### ref Type

`string`

### name

Full name. Max 50 characters.


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/name")

#### name Type

`string`

### shortName

Optional. Shortened name. Max 16 characters.


`shortName`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-area-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopAreaInfo/properties/shortName")

#### shortName Type

`string`

## Definitions group stopPointInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo"}
```

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                         |
| :------------------------------ | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref-3)                   | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/ref")                     |
| [name](#name-6)                 | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/name")                   |
| [shortName](#shortname-4)       | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/shortName")         |
| [designation](#designation-1)   | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/designation")     |
| [localNumber](#localnumber)     | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-localnumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/localNumber")     |
| [length](#length)               | `number` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-length.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/length")               |
| [stopPointKeys](#stoppointkeys) | `array`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-stoppointkeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/stopPointKeys") |

### ref

Id of the Stop Area.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/ref")

#### ref Type

`string`

### name

Full name. Max 50 characters.


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/name")

#### name Type

`string`

### shortName

Optional. Shortened name. Max 16 characters.


`shortName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-shortname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/shortName")

#### shortName Type

`string`

### designation

Optional. Track, gate, stop etc. as shown to the public. This is for local orientation within a stop area, bus terminal or station.


`designation`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-designation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/designation")

#### designation Type

`string`

### localNumber

The display order of stops within a stop area.


`localNumber`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-localnumber.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/localNumber")

#### localNumber Type

`number`

### length

Optional. The stops capacity in meters.


`length`

-   is optional
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-length.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/length")

#### length Type

`number`

### stopPointKeys

Optional. Array with point specific information.


`stopPointKeys`

-   is optional
-   Type: `object[]` ([Key](vehicle-journey-details-definitions-stop-point-info-properties-stoppointkeys-key.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-stop-point-info-properties-stoppointkeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/stopPointInfo/properties/stopPointKeys")

#### stopPointKeys Type

`object[]` ([Key](vehicle-journey-details-definitions-stop-point-info-properties-stoppointkeys-key.md))

## Definitions group arrival

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/arrival"}
```

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                             |
| :-------------------------------- | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [latestDateTime](#latestdatetime) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-latestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/latestDateTime") |
| [arrivalType](#arrivaltype)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-arrivaltype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/arrivalType")       |

### latestDateTime

The latest arrival time expected according to original plan. Arrival after this time is LATE. ISO 8601, UTC.


`latestDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-latestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/latestDateTime")

#### latestDateTime Type

`string`

### arrivalType

Usage of the arrival according to original plan. NoStop and StopNoBoarding means that the departure should NOT be presented public.


`arrivalType`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-arrival-properties-arrivaltype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/arrival/properties/arrivalType")

#### arrivalType Type

`string`

## Definitions group departure

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure"}
```

| Property                              | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                     |
| :------------------------------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [earliestDateTime](#earliestdatetime) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-earliestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/earliestDateTime") |
| [departureType](#departuretype)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-departuretype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/departureType")       |

### earliestDateTime

The earliest permitted departure time according to original plan. Departure before this time is EARLY. ISO 8601, UTC.


`earliestDateTime`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-earliestdatetime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/earliestDateTime")

#### earliestDateTime Type

`string`

### departureType

Usage of the departure according to original plan. NoStop and StopNoAlighting means that the arrival should NOT be presented public.


`departureType`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-departure-properties-departuretype.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/departure/properties/departureType")

#### departureType Type

`string`

## Definitions group organisationInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo"}
```

| Property            | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                |
| :------------------ | -------- | -------- | -------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref-4)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/ref")       |
| [code](#code-1)     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/code")     |
| [name](#name-7)     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/name")     |
| [number](#number-1) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/number") |

### ref

A unique identifier.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/ref")

#### ref Type

`string`

### code

Short abbreviation.


`code`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/code")

#### code Type

`string`

### name

Full name.


`name`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/name")

#### name Type

`string`

### number

The number of the object that the organisation info refers to. Transport Authority number or Contractor Number.


`number`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-organisation-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/organisationInfo/properties/number")

#### number Type

`string`

## Definitions group key

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/key"}
```

| Property                        | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                   |
| :------------------------------ | -------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [deviceName](#devicename)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-devicename.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/key/properties/deviceName")       |
| [typeCode](#typecode)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-typecode.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/key/properties/typeCode")           |
| [parameterData](#parameterdata) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-parameterdata.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/key/properties/parameterData") |

### deviceName

Name of devices for which this key applies.


`deviceName`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-devicename.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/key/properties/deviceName")

#### deviceName Type

`string`

### typeCode

Name of data type.


`typeCode`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-typecode.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/key/properties/typeCode")

#### typeCode Type

`string`

### parameterData

The data formatted in an agreed (that could be customer specific) format for the specified DeviceName and TypeCode.


`parameterData`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-key-properties-parameterdata.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/key/properties/parameterData")

#### parameterData Type

`string`

## Definitions group tariffZoneInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo"}
```

| Property            | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                             |
| :------------------ | -------- | -------- | -------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [ref](#ref-5)       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/ref")       |
| [number](#number-2) | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/number") |
| [Code](#code-2)     | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/Code")     |
| [name](#name-8)     | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/name")     |

### ref

A unique identifier.


`ref`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-ref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/ref")

#### ref Type

`string`

### number

The number of the tariff zone unique within the transport authority.


`number`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-number.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/number")

#### number Type

`string`

### Code

Optional. Short abbreviation.


`Code`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-code.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/Code")

#### Code Type

`string`

### name

Optional. Full name.


`name`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-tariff-zone-info-properties-name.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/tariffZoneInfo/properties/name")

#### name Type

`string`

## Definitions group connectionInfo

Reference this group by using

```json
{"$ref":"https://schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo"}
```

| Property                                              | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                |
| :---------------------------------------------------- | -------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [connectionRef](#connectionref)                       | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-connectionref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/connectionRef")                       |
| [transportModeCode](#transportmodecode-1)             | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-transportmodecode.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/transportModeCode")               |
| [lineAuthorityCode](#lineauthoritycode)               | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-lineauthoritycode.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineAuthorityCode")               |
| [lineDesignation](#linedesignation-1)                 | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-linedesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineDesignation")                   |
| [directionName](#directionname)                       | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-directionname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/directionName")                       |
| [stopAreaName](#stopareaname)                         | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stopareaname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopAreaName")                         |
| [stopPointDesignation](#stoppointdesignation)         | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stoppointdesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopPointDesignation")         |
| [minChangeDurationSeconds](#minchangedurationseconds) | `number` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-minchangedurationseconds.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/minChangeDurationSeconds") |
| [maxWaitingUntilTime](#maxwaitinguntiltime)           | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-maxwaitinguntiltime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/maxWaitingUntilTime")           |

### connectionRef

Identifier used for matching with real-time data in later stage. Is unique in scope of current vehicle journey and call sequenceNumber. Typically has the value of the connecting journeys directionOfLineRef.


`connectionRef`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-connectionref.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/connectionRef")

#### connectionRef Type

`string`

### transportModeCode

The transport mode. Possible values in examples.


`transportModeCode`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-transportmodecode.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/transportModeCode")

#### transportModeCode Type

`string`

#### transportModeCode Examples

```json
"BUS"
```

```json
"TRAM"
```

### lineAuthorityCode

Short abbreviation for the organisation providing the connecting journey. Possible values in examples.


`lineAuthorityCode`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-lineauthoritycode.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineAuthorityCode")

#### lineAuthorityCode Type

`string`

#### lineAuthorityCode Examples

```json
"SJ"
```

```json
"ÖTåg"
```

```json
"SL"
```

### lineDesignation

The public line number displayed to passengers for the connecting journey. Observe that this value can be alphanumeric!


`lineDesignation`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-linedesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/lineDesignation")

#### lineDesignation Type

`string`

### directionName

Optional. Name of direction for connecting journey.


`directionName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-directionname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/directionName")

#### directionName Type

`string`

### stopAreaName

Optional. Name of stop for the connecting journey. Only included if different stop than the stop this vehicle stops at.


`stopAreaName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stopareaname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopAreaName")

#### stopAreaName Type

`string`

### stopPointDesignation

Optional. Platform/track/gate number or letter as shown to the public for the stop of the connecting journey. This is for local orientation within a stop area, bus terminal or station.


`stopPointDesignation`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-stoppointdesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/stopPointDesignation")

#### stopPointDesignation Type

`string`

### minChangeDurationSeconds

The minimum number of seconds needed to transfer (walk) between the involved vehicles. May need to be multiplied by some factors depending on different passenger abilities.


`minChangeDurationSeconds`

-   is required
-   Type: `number`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-minchangedurationseconds.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/minChangeDurationSeconds")

#### minChangeDurationSeconds Type

`number`

### maxWaitingUntilTime

Optional. The date and time when the connection guarantee ends. The fetcher vehicle may leave at this time even if feeder vehicle has not yet arrived. ISO 8601, UTC.


`maxWaitingUntilTime`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-connection-info-properties-maxwaitinguntiltime.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.0/operational-information/vehicle-journey-details.json#/definitions/connectionInfo/properties/maxWaitingUntilTime")

#### maxWaitingUntilTime Type

`string`
