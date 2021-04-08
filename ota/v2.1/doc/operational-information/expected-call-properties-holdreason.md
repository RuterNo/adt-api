# Untitled string in ExpectedCall Schema

```txt
#/properties/holdReason#/properties/holdReason
```

Optional. Only provided if vehicle should hold. Describes the reason why the driver should hold at this stop. Possible values in examples.


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                             |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [expected-call.json\*](../../schema/operational-information/expected-call.json "open original schema") |

## holdReason Type

`string`

## holdReason Examples

```json
"CONNECTION_PROTECTION"
```

```json
"TIMING_POINT"
```

```json
"DRIVER_CHANGE"
```
