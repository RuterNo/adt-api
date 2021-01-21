# [v2.0](../../README.md) / Extended information 
 
# Extended Information

These topics are intended for announcements of adapted passenger information. It is possible to provide multiple topics in parallel with information in different languages
 
 ## [Extended information Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Deviation information](deviation-information.md) | ```{PTO}/ruter/{vehicleID}/ei/deviation_information/```  | ruter-bo | ruter-dpi
[Transfer information](transfer-information.md) | ```{PTO}/ruter/{vehicleID}/ei/expected_call/transfer_information```  | ruter-bo | ruter-dpi
[Due information](due-information.md) | ```{PTO}/ruter/{vehicleID}/ei/expected_call/due_information/```  | ruter-bo | ruter-dpi
[Audio message](audio-message.md) | ```{PTO}/ruter/{vehicleID}/ei/audio_message```  | ruter-bo | ruter-dpi

 --- 

