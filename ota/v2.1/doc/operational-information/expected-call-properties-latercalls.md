# Untitled array in ExpectedCall Schema

```txt
#/properties/laterCalls#/properties/laterCalls
```

Optional. Only provided if there are any calls in the journey after the expected call. Describes a configured number of calls that follow in sequence after the expected call. Note that the first item in the list represents the "next stop" only when the vehicle is standing at a stop. If the vehicle is between stops then the first item represents the first stop after the next stop. The configured max number of later Calls to be expected should be provided in configValue01 for this topic under topic tobs/mi/provider_clients//provided_topics.


| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                                             |
| :------------------ | ---------- | -------------- | ----------------------- | :---------------- | --------------------- | ------------------- | ------------------------------------------------------------------------------------------------------ |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [expected-call.json\*](../../schema/operational-information/expected-call.json "open original schema") |

## laterCalls Type

unknown\[]
