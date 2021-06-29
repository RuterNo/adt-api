# [v2.0](../../README.md) / Driver interaction 
 
# Driver Interaction 
 ## [Driver interaction Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Assignment attempt](assignment-attempt.md) | ```ruter/{PTO}/{vehicleID}/di/assignment_attempt/block```  | Vehicle | Ruter Bo
[Assignment attempt rejection](assignment-attempt-rejection.md) | ```{PTO}/ruter/{vehicleID}/di/assignment_attempt_rejection/block```  | Ruter Bo | Vehicle Avms
[Destination display override](destination-display-override.md) | ```ruter/{PTO}/{vehicleID}/di/override_attempt/destination_display```  | Vehicle | Ruter Dpi
[Available destination displays](available-destination-displays.md) | ```{PTO}/ruter/{vehicleID}/di/available_destination_displays```  | Ruter Bo | Vehicle Avms
[Operational message to driver](operational-message-to-driver.md) | ```{PTO}/ruter/{vehicleID}/di/operational_message_to_driver```  | Ruter Bo | Vehicle Madt

 --- 

