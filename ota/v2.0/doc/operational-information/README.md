# [v2.0](../../README.md) / Operational information 
 
# Operational Information 
 ## [Operational information Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Unique identifier](unique-identifier.md) | ```oi/vehicle/unique_identifier```  | vehicle | ruter-bo,ruter-sales
[Current block](current-block.md) | ```{PTO}/ruter/{vehicleID}/oi/current_block/state```  | ruter-bo | ruter-dpi
[Vehicle journey details](vehicle-journey-details.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/details```  | ruter-bo | ruter-dpi,ruter-sales
[Expected call](expected-call.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/expected_call```  | ruter-bo | ruter-dpi,ruter-sales
[Current destination display](current-destination-display.md) | ```{PTO}/ruter/{vehicleID}/oi/current_destination_display/text```  | ruter-bo | ruter-dpi

 --- 

