# Untitled string in ExpectedCall Schema

```txt
https://schemas.ruter.no/adt/ota/api/v2.1/operational-information/expected-call.json#/definitions/call/properties/restriction
```

Optional. Only provided if boarding or alighting restriction applies based on a combination of planned restrictions and partial journey cancellations. Possible values in examples.


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                             |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [expected-call.json\*](../../schema/operational-information/expected-call.json "open original schema") |

## restriction Type

`string`

## restriction Examples

```json
"NO_BOARDING"
```

```json
"NO_ALIGHTING"
```

```json
"NO_STOP"
```
