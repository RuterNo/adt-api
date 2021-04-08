# Destination Display Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/pointCall/properties/destinationDisplay
```

Optional.


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                 |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [vehicle-journey-details.json\*](../../schema/operational-information/vehicle-journey-details.json "open original schema") |

## destinationDisplay Type

`object` ([Destination Display](vehicle-journey-details-definitions-destination-display.md))

# Destination Display Properties

| Property                                      | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                |
| :-------------------------------------------- | -------- | -------- | -------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [productName](#productname)                   | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-productname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/productName")                   |
| [symbolName](#symbolname)                     | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-symbolname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/symbolName")                     |
| [lineDesignation](#linedesignation)           | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-linedesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/lineDesignation")           |
| [primaryDestination](#primarydestination)     | `string` | Required | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-primarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/primaryDestination")     |
| [secondaryDestination](#secondarydestination) | `string` | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-secondarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/secondaryDestination") |
| [displayKeys](#displaykeys)                   | `array`  | Optional | cannot be null | [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-displaykeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/displayKeys")                   |

## productName

Optional. Name of public transport product.


`productName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-productname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/productName")

### productName Type

`string`

## symbolName

Optional. Controls any symbols in display.


`symbolName`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-symbolname.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/symbolName")

### symbolName Type

`string`

## lineDesignation

Displayed line number.


`lineDesignation`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-linedesignation.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/lineDesignation")

### lineDesignation Type

`string`

## primaryDestination

Names of primary destination.


`primaryDestination`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-primarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/primaryDestination")

### primaryDestination Type

`string`

## secondaryDestination

Optional. Names of secondary destination.


`secondaryDestination`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-secondarydestination.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/secondaryDestination")

### secondaryDestination Type

`string`

## displayKeys

Optional. Contains device specific information such as sign codes etcetera. See 5.6.20. A numeric sign code representing the combined destination display information could thus be provided in a contained key with appropriate parameterData. E.g. “Destination=659” It is possible to provide information for multiple display devices in parallel if there is a mixed fleet with different hardware by providing multiple Keys in parallel. E.g. one Key with "deviceName": "SIGN_X" and another Key with "deviceName": "SIGN_Y".


`displayKeys`

-   is optional
-   Type: `object[]` ([Key](vehicle-journey-details-definitions-key.md))
-   cannot be null
-   defined in: [VehicleJourneyDetails](vehicle-journey-details-definitions-destination-display-properties-displaykeys.md "https&#x3A;//schemas.ruter.no/adt/ota/api/v2.1/operational-information/vehicle-journey-details.json#/definitions/destinationDisplay/properties/displayKeys")

### displayKeys Type

`object[]` ([Key](vehicle-journey-details-definitions-key.md))
