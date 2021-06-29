# [v2.0](../../README.md) / Sensor 
 
# Sensor 
 ## [Sensor Schema](README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Stop button](stop-button.md) | ```ruter/{PTO}/{vehicleID}/sensors/stop_button```  | Vehicle | Ruter Bo
[Door](door.md) | ```ruter/{PTO}/{vehicleID}/sensors/door```  | Vehicle | Ruter Bo
[Location](location.md) | ```ruter/{PTO}/{vehicleID}/sensors/gnss/location```  | Vehicle | Ruter Bo
[Odometer](odometer.md) | ```ruter/{PTO}/{vehicleID}/sensors/odometer```  | Vehicle | Ruter Bo
[Clock](clock.md) | ```sensors/clock```  | Vehicle | Vehicle, Ruter Sales
[Apc sensors](apc-sensors.md) | ```ruter/{PTO}/{vehicleID}/sensors/apc_sensors```  | Vehicle | Ruter Bo
[Telemetry](telemetry.md) | ```ruter/{PTO}/{vehicleID}/sensors/telemetry```  | Vehicle | Ruter Bo

 --- 

