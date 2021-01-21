# [v2.0](../../README.md) / Proprietary extensions 
 
# Proprietary Extensions 
 ## [Proprietary extensions Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Sales validation](sales-validation.md) | ```{PTO}/ruter/{vehicleID}/pe/sales_validation```  | ruter-sales | ruter-bo
[Dpi command](dpi-command.md) | ```{PTO}/ruter/{vehicleID}/pe/dpi_command```  | ruter-dpi | ruter-bo
[Dpi diagnostics](dpi-diagnostics.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_diagnostics```  | ruter-dpi | ruter-bo
[Dpi acknowledge](dpi-acknowledge.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_ack```  | vehicle | ruter-bo
[Doors individually](doors-individually.md) | ```ruter/{PTO}/{vehicleID}/pe/doors_individually```  | vehicle | ruter-bo
[Traffic signal priority](traffic-signal-priority.md) | ```{PTO}/ruter/{vehicleID}/pe/tsp```  | ruter-bo | vehicle-tsp

 --- 

