# [v2.0](../../README.md) / Driver interaction 
 
# Driver Interaction 
 ## [Driver interaction Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Assignment attempt](assignment-attempt.md) | ```ruter/{PTO}/{vehicleID}/di/assignment_attempt/block```  | vehicle | ruter-bo
[Assignment attempt rejection](assignment-attempt-rejection.md) | ```{PTO}/ruter/{vehicleID}/di/assignment_attempt_rejection/block```  | ruter-bo | vehicle-avms
[Destination display override](destination-display-override.md) | ```ruter/{PTO}/{vehicleID}/di/override_attempt/destination_display```  | vehicle | ruter-dpi
[Available destination displays](available-destination-displays.md) | ```{PTO}/ruter/{vehicleID}/di/available_destination_displays```  | ruter-bo | vehicle-avms
[Operational message to driver](operational-message-to-driver.md) | ```{PTO}/ruter/{vehicleID}/di/operational_message_to_driver```  | ruter-bo | vehicle-madt

 --- 

