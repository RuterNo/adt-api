# Situation Message Schema

```txt
#/properties/situationMessages#/properties/situationMessages/items
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                         |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :----------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [deviation-information.json*](../../schema/extended-information/deviation-information.json "open original schema") |

## items Type

`object` ([Situation Message](deviation-information-properties-situation-messages-situation-message.md))

# items Properties

| Property            | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                  |
| :------------------ | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [heading](#heading) | `string` | Required | cannot be null | [DeviationInformation](deviation-information-properties-situation-messages-situation-message-properties-heading.md "#/properties/situationMessages#/properties/situationMessages/items/properties/heading") |
| [body](#body)       | `string` | Required | cannot be null | [DeviationInformation](deviation-information-properties-situation-messages-situation-message-properties-body.md "#/properties/situationMessages#/properties/situationMessages/items/properties/body")       |

## heading

The message heading text

`heading`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DeviationInformation](deviation-information-properties-situation-messages-situation-message-properties-heading.md "#/properties/situationMessages#/properties/situationMessages/items/properties/heading")

### heading Type

`string`

## body

The message body text

`body`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [DeviationInformation](deviation-information-properties-situation-messages-situation-message-properties-body.md "#/properties/situationMessages#/properties/situationMessages/items/properties/body")

### body Type

`string`
