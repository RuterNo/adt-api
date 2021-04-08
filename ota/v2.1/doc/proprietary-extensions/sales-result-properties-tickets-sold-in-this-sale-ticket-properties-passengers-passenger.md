# Passenger Schema

```txt
#/properties/tickets/items/properties/passengers/items#/properties/tickets/items/properties/passengers/items
```




| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                          |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | --------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [sales-result.json\*](../../schema/proprietary-extensions/sales-result.json "open original schema") |

## items Type

`object` ([Passenger](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger.md))

# Passenger Properties

| Property                                  | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                                                                                                           |
| :---------------------------------------- | --------- | -------- | -------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [numberOfPassengers](#numberofpassengers) | `integer` | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger-properties-numberofpassengers.md "\#/properties/tickets/items/properties/passengers/items/properties/numberOfPassengers#/properties/tickets/items/properties/passengers/items/properties/numberOfPassengers") |
| [productId](#productid)                   | `integer` | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger-properties-productid.md "\#/properties/tickets/items/properties/passengers/items/properties/productId#/properties/tickets/items/properties/passengers/items/properties/productId")                            |
| [profileId](#profileid)                   | `integer` | Required | cannot be null | [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger-properties-profileid.md "\#/properties/tickets/items/properties/passengers/items/properties/profileId#/properties/tickets/items/properties/passengers/items/properties/profileId")                            |

## numberOfPassengers

Quantity of this passenger


`numberOfPassengers`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger-properties-numberofpassengers.md "\#/properties/tickets/items/properties/passengers/items/properties/numberOfPassengers#/properties/tickets/items/properties/passengers/items/properties/numberOfPassengers")

### numberOfPassengers Type

`integer`

## productId

Product ID of this passenger


`productId`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger-properties-productid.md "\#/properties/tickets/items/properties/passengers/items/properties/productId#/properties/tickets/items/properties/passengers/items/properties/productId")

### productId Type

`integer`

## profileId

Profile ID of this passenger


`profileId`

-   is required
-   Type: `integer`
-   cannot be null
-   defined in: [SalesResult](sales-result-properties-tickets-sold-in-this-sale-ticket-properties-passengers-passenger-properties-profileid.md "\#/properties/tickets/items/properties/passengers/items/properties/profileId#/properties/tickets/items/properties/passengers/items/properties/profileId")

### profileId Type

`integer`
