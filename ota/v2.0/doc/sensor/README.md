# [v2.0](../../README.md) / Sensor 
 
# Sensor 
 ## [Sensor Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Stop button](stop-button.md) | ```ruter/{PTO}/{vehicleID}/sensors/stop_button```  | vehicle | ruter-bo
[Door](door.md) | ```ruter/{PTO}/{vehicleID}/sensors/door```  | vehicle | ruter-bo
[Location](location.md) | ```ruter/{PTO}/{vehicleID}/sensors/gnss/location```  | vehicle | ruter-bo
[Odometer](odometer.md) | ```ruter/{PTO}/{vehicleID}/sensors/odometer```  | vehicle | ruter-bo
[Clock](clock.md) | ```sensors/clock```  | vehicle | vehicle,ruter-sales
[Apc sensors](apc-sensors.md) | ```ruter/{PTO}/{vehicleID}/sensors/apc_sensors```  | vehicle | ruter-bo
[Telemetry](telemetry.md) | ```ruter/{PTO}/{vehicleID}/sensors/telemetry```  | vehicle | ruter-bo

 --- 

