# [v2.0](../../README.md) / Proprietary extensions 
 
# Proprietary Extensions 
 ## [Proprietary extensions Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Sales validation](sales-validation.md) | ```{PTO}/ruter/{vehicleID}/pe/sales_validation```  | Ruter Sales | Ruter Bo
[Dpi command](dpi-command.md) | ```{PTO}/ruter/{vehicleID}/pe/dpi_command```  | Ruter Dpi | Ruter Bo
[Dpi diagnostics](dpi-diagnostics.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_diagnostics```  | Ruter Dpi | Ruter Bo
[Dpi acknowledge](dpi-acknowledge.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_ack```  | Vehicle | Ruter Bo
[Doors individually](doors-individually.md) | ```ruter/{PTO}/{vehicleID}/pe/doors_individually```  | Vehicle | Ruter Bo
[Traffic signal priority](traffic-signal-priority.md) | ```{PTO}/ruter/{vehicleID}/pe/tsp```  | Ruter Bo | Vehicle Tsp

 --- 

