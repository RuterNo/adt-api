# InspectionResult Schema

```txt
#/properties/inspectionResult#/properties/inspectionResult
```

The result of the inspection


| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                                                |
| :------------------ | ---------- | -------------- | ------------ | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [sales-validation-result.json\*](../../schema/proprietary-extensions/sales-validation-result.json "open original schema") |

## inspectionResult Type

`object` ([InspectionResult](sales-validation-result-properties-inspectionresult.md))

# InspectionResult Properties

| Property              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                             |
| :-------------------- | --------- | -------- | -------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [code](#code)         | `integer` | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-inspectionresult-properties-validity-code-returned-by-nod.md "\#/properties/inspectionResult/properties/code#/properties/inspectionResult/properties/code") |
| [message](#message)   | `string`  | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-inspectionresult-properties-message.md "\#/properties/inspectionResult/properties/message#/properties/inspectionResult/properties/message")                 |
| [validity](#validity) | `string`  | Required | cannot be null | [SalesValidationResult](sales-validation-result-properties-inspectionresult-properties-validity.md "\#/properties/inspectionResult/properties/validity#/properties/inspectionResult/properties/validity")              |

## code




`code`

-   is required
-   Type: `integer` ([Validity code returned by NOD](sales-validation-result-properties-inspectionresult-properties-validity-code-returned-by-nod.md))
-   cannot be null
-   defined in: [SalesValidationResult](sales-validation-result-properties-inspectionresult-properties-validity-code-returned-by-nod.md "\#/properties/inspectionResult/properties/code#/properties/inspectionResult/properties/code")

### code Type

`integer` ([Validity code returned by NOD](sales-validation-result-properties-inspectionresult-properties-validity-code-returned-by-nod.md))

## message

Message to be displayed to user


`message`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [SalesValidationResult](sales-validation-result-properties-inspectionresult-properties-message.md "\#/properties/inspectionResult/properties/message#/properties/inspectionResult/properties/message")

### message Type

`string`

## validity

Can be either VALID or INVALID, might change in the future (by for example adding an UNKNOWN for students/seniors)


`validity`

-   is required
-   Type: `string`
-   cannot be null
-   defined in: [SalesValidationResult](sales-validation-result-properties-inspectionresult-properties-validity.md "\#/properties/inspectionResult/properties/validity#/properties/inspectionResult/properties/validity")

### validity Type

`string`

### validity Examples

```json
"VALID"
```

```json
"INVALID"
```
