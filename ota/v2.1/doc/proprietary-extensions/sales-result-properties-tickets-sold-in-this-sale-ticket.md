# Ticket Schema

```txt
#/properties/tickets/items#/properties/tickets/items
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                          |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | --------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [sales-result.json\*](../../schema/proprietary-extensions/sales-result.json "open original schema") |

## items Type

`object` ([Ticket](sales-result-properties-tickets-sold-in-this-sale-ticket.md))

# Ticket Properties

| Property                                  | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                   |
| :---------------------------------------- | --------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [numberOfZonesToPay](#numberofzonestopay) | `integer` | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-numberofzonestopay.md "\#/properties/tickets/items/properties/numberOfZonesToPay#/properties/tickets/items/properties/numberOfZonesToPay") |
| [passengers](#passengers)                 | `array`   | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers.md "\#/properties/tickets/items/properties/passengers#/properties/tickets/items/properties/passengers")                         |
| [price](#price)                           | `integer` | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-price.md "\#/properties/tickets/items/properties/price#/properties/tickets/items/properties/price")                                        |
| [startDate](#startdate)                   | `string`  | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-startdate.md "\#/properties/tickets/items/properties/startDate#/properties/tickets/items/properties/startDate")                            |
| [zoneFrom](#zonefrom)                     | `string`  | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-zonefrom.md "\#/properties/tickets/items/properties/zoneFrom#/properties/tickets/items/properties/zoneFrom")                               |
| [zoneTo](#zoneto)                         | `string`  | Required | can be null    | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-zoneto.md "\#/properties/tickets/items/properties/zoneTo#/properties/tickets/items/properties/zoneTo")                                     |
| [zoneVia](#zonevia)                       | `string`  | Required | can be null    | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-zonevia.md "\#/properties/tickets/items/properties/zoneVia#/properties/tickets/items/properties/zoneVia")                                  |
| [externalID](#externalid)                 | `string`  | Optional | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-externalid.md "\#/properties/tickets/items/properties/externalID#/properties/tickets/items/properties/externalID")                         |
| [productTemplateID](#producttemplateid)   | `integer` | Optional | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-producttemplateid.md "\#/properties/tickets/items/properties/productTemplateID#/properties/tickets/items/properties/productTemplateID")    |
| [selectedZones](#selectedzones)           | `array`   | Required | can be null    | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-selectedzones.md "\#/properties/tickets/items/properties/selectedZones#/properties/tickets/items/properties/selectedZones")                |

## numberOfZonesToPay

Number of zones to pay for


`numberOfZonesToPay`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-numberofzonestopay.md "\#/properties/tickets/items/properties/numberOfZonesToPay#/properties/tickets/items/properties/numberOfZonesToPay")

### numberOfZonesToPay Type

`integer`

## passengers

Passengers in this ticket


`passengers`

-   is required
-   Type: `object[]` ([Passenger](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger.md))
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers.md "\#/properties/tickets/items/properties/passengers#/properties/tickets/items/properties/passengers")

### passengers Type

`object[]` ([Passenger](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger.md))

## price

price of ticket (in øre)


`price`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-price.md "\#/properties/tickets/items/properties/price#/properties/tickets/items/properties/price")

### price Type

`integer`

## startDate

ISO 8601, UTC


`startDate`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-startdate.md "\#/properties/tickets/items/properties/startDate#/properties/tickets/items/properties/startDate")

### startDate Type

`string`

## zoneFrom

Start zone name


`zoneFrom`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-zonefrom.md "\#/properties/tickets/items/properties/zoneFrom#/properties/tickets/items/properties/zoneFrom")

### zoneFrom Type

`string`

## zoneTo

Destination zone name


`zoneTo`

-   is required
-   Type: `string`
-   can be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-zoneto.md "\#/properties/tickets/items/properties/zoneTo#/properties/tickets/items/properties/zoneTo")

### zoneTo Type

`string`

## zoneVia

Via zone name


`zoneVia`

-   is required
-   Type: `string`
-   can be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-zonevia.md "\#/properties/tickets/items/properties/zoneVia#/properties/tickets/items/properties/zoneVia")

### zoneVia Type

`string`

## externalID

Ruter Sales Client reference to ticket


`externalID`

-   is optional
-   Type: `string`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-externalid.md "\#/properties/tickets/items/properties/externalID#/properties/tickets/items/properties/externalID")

### externalID Type

`string`

## productTemplateID

Type of ticket


`productTemplateID`

-   is optional
-   Type: `integer`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-producttemplateid.md "\#/properties/tickets/items/properties/productTemplateID#/properties/tickets/items/properties/productTemplateID")

### productTemplateID Type

`integer`

## selectedZones

Array of zones of underlying ticket (for additional tickets only)


`selectedZones`

-   is required
-   Type: `string[]`
-   can be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-selectedzones.md "\#/properties/tickets/items/properties/selectedZones#/properties/tickets/items/properties/selectedZones")

### selectedZones Type

`string[]`
