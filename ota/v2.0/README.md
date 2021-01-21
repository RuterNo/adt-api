# API v. 2.0

## Schemas for ADT OTA API

# Overview

This API description covers [Ruter’s ADT agreement v2.0](https://ruter.atlassian.net/wiki/spaces/DS/pages/231178249 "https://ruter.atlassian.net/wiki/spaces/DS/pages/231178249"). The API describes a set of MQTT topics which are used to distribute data onboard public transport vehicles/vessels as well as between the vehicle/vessel and Ruter’s Back Office or vv.


## Upgrades to the API

The API follows the upgrade cycles of ADT. Major releases are done more or less once a year and usually include breaking changes.

Minor/build releases are performed as continual deliveries and are non-breaking. New versions of this document will be published when new topics and/or fields are added.

## Consumer Client Requirements

Clients consuming information posted on the topics must be tolerant to:

*   That optional properties can be null or left out.

*   That arrays can contain any number of elements including zero.

*   That returned data can be extended with new properties without notice.

## Quality of Service, Retained Flag and Persistence


The listed topics are topics that are to be produced in either the vehicle or in the Ruter Back Office.

All data must be JSON and UTF-8 encoded.

Topics are categorized by a thematic perspective, according to the topic structure proposed for ITxPT at the time of writing.

## Translation of topic names

Global topic names are generally written on the format of _\<recipient\>/\<sender\>/\<vehicleid\>/\<topic\>_ to make it easy to identify the source and destination of the messages.

Local topic names have omitted the _\<recipient\>/\<sender\>/\<vehicleid\>_ part in order to have onboard equipment pre-configured with vehicle independent settings.

All topic names must thus be rewritten local/global in the MQTT bridge according to a provided configuration file.

# List of topics
 
 ## [Driver interaction Schema](./doc/driver-interaction/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Assignment attempt](./doc/driver-interaction/assignment-attempt.md) | ```ruter/{PTO}/{vehicleID}/di/assignment_attempt/block```  | vehicle | ruter-bo
[Assignment attempt rejection](./doc/driver-interaction/assignment-attempt-rejection.md) | ```{PTO}/ruter/{vehicleID}/di/assignment_attempt_rejection/block```  | ruter-bo | vehicle-avms
[Destination display override](./doc/driver-interaction/destination-display-override.md) | ```ruter/{PTO}/{vehicleID}/di/override_attempt/destination_display```  | vehicle | ruter-dpi
[Available destination displays](./doc/driver-interaction/available-destination-displays.md) | ```{PTO}/ruter/{vehicleID}/di/available_destination_displays```  | ruter-bo | vehicle-avms
[Operational message to driver](./doc/driver-interaction/operational-message-to-driver.md) | ```{PTO}/ruter/{vehicleID}/di/operational_message_to_driver```  | ruter-bo | vehicle-madt

 --- 

 
 ## [Extended information Schema](./doc/extended-information/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Deviation information](./doc/extended-information/deviation-information.md) | ```{PTO}/ruter/{vehicleID}/ei/deviation_information/```  | ruter-bo | ruter-dpi
[Transfer information](./doc/extended-information/transfer-information.md) | ```{PTO}/ruter/{vehicleID}/ei/expected_call/transfer_information```  | ruter-bo | ruter-dpi
[Due information](./doc/extended-information/due-information.md) | ```{PTO}/ruter/{vehicleID}/ei/expected_call/due_information/```  | ruter-bo | ruter-dpi
[Audio message](./doc/extended-information/audio-message.md) | ```{PTO}/ruter/{vehicleID}/ei/audio_message```  | ruter-bo | ruter-dpi

 --- 

 
 ## [Operational information Schema](./doc/operational-information/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Unique identifier](./doc/operational-information/unique-identifier.md) | ```oi/vehicle/unique_identifier```  | vehicle | ruter-bo,ruter-sales
[Current block](./doc/operational-information/current-block.md) | ```{PTO}/ruter/{vehicleID}/oi/current_block/state```  | ruter-bo | ruter-dpi
[Vehicle journey details](./doc/operational-information/vehicle-journey-details.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/details```  | ruter-bo | ruter-dpi,ruter-sales
[Expected call](./doc/operational-information/expected-call.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/expected_call```  | ruter-bo | ruter-dpi,ruter-sales
[Current destination display](./doc/operational-information/current-destination-display.md) | ```{PTO}/ruter/{vehicleID}/oi/current_destination_display/text```  | ruter-bo | ruter-dpi

 --- 

 
 ## [Proprietary extensions Schema](./doc/proprietary-extensions/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Sales validation](./doc/proprietary-extensions/sales-validation.md) | ```{PTO}/ruter/{vehicleID}/pe/sales_validation```  | ruter-sales | ruter-bo
[Dpi command](./doc/proprietary-extensions/dpi-command.md) | ```{PTO}/ruter/{vehicleID}/pe/dpi_command```  | ruter-dpi | ruter-bo
[Dpi diagnostics](./doc/proprietary-extensions/dpi-diagnostics.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_diagnostics```  | ruter-dpi | ruter-bo
[Dpi acknowledge](./doc/proprietary-extensions/dpi-acknowledge.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_ack```  | vehicle | ruter-bo
[Doors individually](./doc/proprietary-extensions/doors-individually.md) | ```ruter/{PTO}/{vehicleID}/pe/doors_individually```  | vehicle | ruter-bo
[Traffic signal priority](./doc/proprietary-extensions/traffic-signal-priority.md) | ```{PTO}/ruter/{vehicleID}/pe/tsp```  | ruter-bo | vehicle-tsp

 --- 

 
 ## [Sensor Schema](./doc/sensor/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Stop button](./doc/sensor/stop-button.md) | ```ruter/{PTO}/{vehicleID}/sensors/stop_button```  | vehicle | ruter-bo
[Door](./doc/sensor/door.md) | ```ruter/{PTO}/{vehicleID}/sensors/door```  | vehicle | ruter-bo
[Location](./doc/sensor/location.md) | ```ruter/{PTO}/{vehicleID}/sensors/gnss/location```  | vehicle | ruter-bo
[Odometer](./doc/sensor/odometer.md) | ```ruter/{PTO}/{vehicleID}/sensors/odometer```  | vehicle | ruter-bo
[Clock](./doc/sensor/clock.md) | ```sensors/clock```  | vehicle | vehicle,ruter-sales
[Apc sensors](./doc/sensor/apc-sensors.md) | ```ruter/{PTO}/{vehicleID}/sensors/apc_sensors```  | vehicle | ruter-bo
[Telemetry](./doc/sensor/telemetry.md) | ```ruter/{PTO}/{vehicleID}/sensors/telemetry```  | vehicle | ruter-bo

 --- 

