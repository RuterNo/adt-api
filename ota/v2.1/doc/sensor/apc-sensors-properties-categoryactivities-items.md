# Untitled object in ApcSensors Schema

```txt
#/properties/categoryActivities#/properties/categoryActivities/items
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                       |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [apc-sensors.json*](../../schema/sensor/apc-sensors.json "open original schema") |

## items Type

`object` ([Details](apc-sensors-properties-categoryactivities-items.md))

# items Properties

| Property                          | Type     | Required | Nullable       | Defined by                                                                                                                                                                                  |
| :-------------------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [categoryRef](#categoryref)       | `string` | Required | cannot be null | [ApcSensors](apc-sensors-properties-categoryactivities-items-properties-categoryref.md "#/properties/categoryActivities#/properties/categoryActivities/items/properties/categoryRef")       |
| [alightingCount](#alightingcount) | `number` | Required | cannot be null | [ApcSensors](apc-sensors-properties-categoryactivities-items-properties-alightingcount.md "#/properties/categoryActivities#/properties/categoryActivities/items/properties/alightingCount") |
| [boardingCount](#boardingcount)   | `number` | Required | cannot be null | [ApcSensors](apc-sensors-properties-categoryactivities-items-properties-boardingcount.md "#/properties/categoryActivities#/properties/categoryActivities/items/properties/boardingCount")   |

## categoryRef

Object class reference. Possible values given in examples.

`categoryRef`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [ApcSensors](apc-sensors-properties-categoryactivities-items-properties-categoryref.md "#/properties/categoryActivities#/properties/categoryActivities/items/properties/categoryRef")

### categoryRef Type

`string`

### categoryRef Examples

```json
"ADULT"
```

```json
"CHILD"
```

```json
"PRAM"
```

```json
"BIKE"
```

```json
"WHEELCHAIR"
```

## alightingCount

Accumulated number of alighting of this category detected by this sensor since last reset.

`alightingCount`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [ApcSensors](apc-sensors-properties-categoryactivities-items-properties-alightingcount.md "#/properties/categoryActivities#/properties/categoryActivities/items/properties/alightingCount")

### alightingCount Type

`number`

## boardingCount

Accumulated number of boarding of this category detected by this sensor since last reset.

`boardingCount`

*   is required

*   Type: `number`

*   cannot be null

*   defined in: [ApcSensors](apc-sensors-properties-categoryactivities-items-properties-boardingcount.md "#/properties/categoryActivities#/properties/categoryActivities/items/properties/boardingCount")

### boardingCount Type

`number`
