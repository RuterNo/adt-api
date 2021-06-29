# [v2.0](../../README.md) / Operational information 
 
# Operational Information 
 ## [Operational information Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Unique identifier](unique-identifier.md) | ```oi/vehicle/unique_identifier```  | Vehicle | Ruter Bo, Ruter Sales
[Current block](current-block.md) | ```{PTO}/ruter/{vehicleID}/oi/current_block/state```  | Ruter Bo | Ruter Dpi
[Vehicle journey details](vehicle-journey-details.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/details```  | Ruter Bo | Ruter Dpi, Ruter Sales
[Expected call](expected-call.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/expected_call```  | Ruter Bo | Ruter Dpi, Ruter Sales
[Current destination display](current-destination-display.md) | ```{PTO}/ruter/{vehicleID}/oi/current_destination_display/text```  | Ruter Bo | Ruter Dpi

 --- 

