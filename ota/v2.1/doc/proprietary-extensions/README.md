# [v2.1](../../README.md) / Proprietary extensions 
 
# Proprietary Extensions 
 ## [Proprietary extensions Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Dpi extensions from vehicle](dpi-extensions-from-vehicle.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi/#```  | Vehicle Dpi | Ruter Dpi
[Dpi extensions from ruter](dpi-extensions-from-ruter.md) | ```{PTO}/ruter/{vehicleID}/pe/dpi/#```  | Ruter Dpi | Vehicle Dpi
[Sales diagnostics](sales-diagnostics.md) | ```ruter/{PTO}/{vehicleID}/pe/sales/diagnostics```  | Ruter Sales | Ruter Bo
[Sales validation result](sales-validation-result.md) | ```ruter/{PTO}/{vehicleID}/pe/sales/validationresult```  | Ruter Sales | Ruter Bo
[Sales result](sales-result.md) | ```ruter/{PTO}/{vehicleID}/pe/sales/saleresult```  | Ruter Sales | Ruter Bo
[Door lock](door-lock.md) | ```ruter/{PTO}/{vehicleID}/pe/doorlock```  | Vehicle | Ruter Bo, Vehicle Dpi
[Active cab](active-cab.md) | ```ruter/{PTO}/{vehicleID}/pe/activecab```  | Vehicle | Ruter Bo, Vehicle Dpi
[Sales validation](sales-validation.md) | ```{PTO}/ruter/{vehicleID}/pe/sales_validation```  | Ruter Sales | Ruter Bo
[Dpi command](dpi-command.md) | ```{PTO}/ruter/{vehicleID}/pe/dpi_command```  | Ruter Dpi | Ruter Bo
[Dpi diagnostics](dpi-diagnostics.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_diagnostics```  | Ruter Dpi | Ruter Bo
[Dpi acknowledge](dpi-acknowledge.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_ack```  | Vehicle | Ruter Bo
[Doors individually](doors-individually.md) | ```ruter/{PTO}/{vehicleID}/pe/doors_individually```  | Vehicle | Ruter Bo
[Traffic signal priority](traffic-signal-priority.md) | ```{PTO}/ruter/{vehicleID}/pe/tsp```  | Ruter Bo | Vehicle Tsp

 --- 

