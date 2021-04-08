# API v. 2.1

## Overview
This API description covers Ruter’s ADT agreement v2.1 [Ruter’s ADT agreement v2.1](https://ruter.atlassian.net/wiki/spaces/DS/pages/953483265 "https://ruter.atlassian.net/wiki/spaces/DS/pages/953483265"). The API describes a set of MQTT topics which are used to distribute data onboard public transport vehicles/vessels as well as between the vehicle/vessel and Ruter’s Back Office or vv.

### Upgrades to the API
The API follows the upgrade cycles of ADT. Major releases are done more or less once a year and usually include breaking changes.

Minor/build releases are performed as continual deliveries and are non-breaking. New versions of this document will be published when new topics and/or fields are added.

Minor changes in the document are flagged either by color, or by specifying (NEW) in the heading.

Note: Corrections of unfortunate misspellings or other obvious flaws may occur - but are not considered as upgrades.

### Consumer Client Requirements
Clients consuming information posted on the topics must be tolerant to:
- That optional properties can be null or left out.
- That arrays can contain any number of elements including zero.
- That returned data can be extended with new properties without notice.

### Quality of Service, Retained Flag and Persistence
Generally, QoS level 1 is applied for most topics and the retain flag is true for most topics. See the respective topic for precise info.

Subscribers should start with Clean Session set to True to assure that they get the latest information at reconnection (the retained info) and avoid first having to process a long queue of outdated old information that in reality hinders new relevant information to reach the subscriber.

### Translation of topic names
Global topic names are generally written on the format of `{recipient}/{sender}/{vehicleid}/{topic}` to make it easy to identify the source and destination of the messages.

Local topic names have omitted the `{recipient}/{sender}/{vehicleid}` part in order to have onboard equipment pre-configured with vehicle independent settings.

All topic names must thus be rewritten local/global in the MQTT bridge according to a provided configuration file.
### List of topics
The listed topics are topics that are to be produced in either the vehicle or in the Ruter Back Office.

All data must be JSON and UTF-8 encoded.

Topics are categorized by a thematic perspective, according to the topic structure proposed for ITxPT at the time of writing.
 
 ## [Driver interaction Schema](./doc/driver-interaction/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Assignment attempt](./doc/driver-interaction/assignment-attempt.md) | ```ruter/{PTO}/{vehicleID}/di/assignment_attempt/block```  | Vehicle | Ruter Bo
[Assignment attempt rejection](./doc/driver-interaction/assignment-attempt-rejection.md) | ```{PTO}/ruter/{vehicleID}/di/assignment_attempt_rejection/block```  | Ruter Bo | Vehicle Avms
[Destination display override](./doc/driver-interaction/destination-display-override.md) | ```ruter/{PTO}/{vehicleID}/di/override_attempt/destination_display```  | Vehicle | Ruter Dpi
[Available destination displays](./doc/driver-interaction/available-destination-displays.md) | ```{PTO}/ruter/{vehicleID}/di/available_destination_displays```  | Ruter Bo | Vehicle Avms
[Operational message to driver](./doc/driver-interaction/operational-message-to-driver.md) | ```{PTO}/ruter/{vehicleID}/di/operational_message_to_driver```  | Ruter Bo | Vehicle Madt

 --- 

 
 ## [Extended information Schema](./doc/extended-information/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Deviation information](./doc/extended-information/deviation-information.md) | ```{PTO}/ruter/{vehicleID}/ei/deviation_information/```  | Ruter Bo | Ruter Dpi
[Transfer information](./doc/extended-information/transfer-information.md) | ```{PTO}/ruter/{vehicleID}/ei/expected_call/transfer_information```  | Ruter Bo | Ruter Dpi
[Due information](./doc/extended-information/due-information.md) | ```{PTO}/ruter/{vehicleID}/ei/expected_call/due_information/```  | Ruter Bo | Ruter Dpi
[Audio message](./doc/extended-information/audio-message.md) | ```{PTO}/ruter/{vehicleID}/ei/audio_message```  | Ruter Bo | Ruter Dpi

 --- 

 
 ## [Operational information Schema](./doc/operational-information/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Unique identifier](./doc/operational-information/unique-identifier.md) | ```oi/vehicle/unique_identifier```  | Vehicle | Ruter Bo, Ruter Sales
[Current block](./doc/operational-information/current-block.md) | ```{PTO}/ruter/{vehicleID}/oi/current_block/state```  | Ruter Bo | Ruter Dpi
[Vehicle journey details](./doc/operational-information/vehicle-journey-details.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/details```  | Ruter Bo | Ruter Dpi, Ruter Sales
[Expected call](./doc/operational-information/expected-call.md) | ```{PTO}/ruter/{vehicleID}/oi/current_vehicle_journey/expected_call```  | Ruter Bo | Ruter Dpi, Ruter Sales
[Current destination display](./doc/operational-information/current-destination-display.md) | ```{PTO}/ruter/{vehicleID}/oi/current_destination_display/text```  | Ruter Bo | Ruter Dpi

 --- 

 
 ## [Proprietary extensions Schema](./doc/proprietary-extensions/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Dpi extensions from vehicle](./doc/proprietary-extensions/dpi-extensions-from-vehicle.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi/#```  | Vehicle Dpi | Ruter Dpi
[Dpi extensions from ruter](./doc/proprietary-extensions/dpi-extensions-from-ruter.md) | ```{PTO}/ruter/{vehicleID}/pe/dpi/#```  | Ruter Dpi | Vehicle Dpi
[Sales diagnostics](./doc/proprietary-extensions/sales-diagnostics.md) | ```ruter/{PTO}/{vehicleID}/pe/sales/diagnostics```  | Ruter Sales | Ruter Bo
[Sales validation result](./doc/proprietary-extensions/sales-validation-result.md) | ```ruter/{PTO}/{vehicleID}/pe/sales/validationresult```  | Ruter Sales | Ruter Bo
[Sales result](./doc/proprietary-extensions/sales-result.md) | ```ruter/{PTO}/{vehicleID}/pe/sales/saleresult```  | Ruter Sales | Ruter Bo
[Door lock](./doc/proprietary-extensions/door-lock.md) | ```ruter/{PTO}/{vehicleID}/pe/doorlock```  | Vehicle | Ruter Bo, Vehicle Dpi
[Active cab](./doc/proprietary-extensions/active-cab.md) | ```ruter/{PTO}/{vehicleID}/pe/activecab```  | Vehicle | Ruter Bo, Vehicle Dpi
[Sales validation](./doc/proprietary-extensions/sales-validation.md) | ```{PTO}/ruter/{vehicleID}/pe/sales_validation```  | Ruter Sales | Ruter Bo
[Dpi command](./doc/proprietary-extensions/dpi-command.md) | ```{PTO}/ruter/{vehicleID}/pe/dpi_command```  | Ruter Dpi | Ruter Bo
[Dpi diagnostics](./doc/proprietary-extensions/dpi-diagnostics.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_diagnostics```  | Ruter Dpi | Ruter Bo
[Dpi acknowledge](./doc/proprietary-extensions/dpi-acknowledge.md) | ```ruter/{PTO}/{vehicleID}/pe/dpi_ack```  | Vehicle | Ruter Bo
[Doors individually](./doc/proprietary-extensions/doors-individually.md) | ```ruter/{PTO}/{vehicleID}/pe/doors_individually```  | Vehicle | Ruter Bo
[Traffic signal priority](./doc/proprietary-extensions/traffic-signal-priority.md) | ```{PTO}/ruter/{vehicleID}/pe/tsp```  | Ruter Bo | Vehicle Tsp

 --- 

 
 ## [Sensor Schema](./doc/sensor/README.md) 
 
Schema                                | MQTT topic                                                               | Produced by | Consumed by 
| :---------------------------------- | :----------------------------------------------------------------------- | ----------- | -------- |
[Stop button](./doc/sensor/stop-button.md) | ```ruter/{PTO}/{vehicleID}/sensors/stop_button```  | Vehicle | Ruter Bo
[Door](./doc/sensor/door.md) | ```ruter/{PTO}/{vehicleID}/sensors/door```  | Vehicle | Ruter Bo
[Location](./doc/sensor/location.md) | ```ruter/{PTO}/{vehicleID}/sensors/gnss/location```  | Vehicle | Ruter Bo
[Odometer](./doc/sensor/odometer.md) | ```ruter/{PTO}/{vehicleID}/sensors/odometer```  | Vehicle | Ruter Bo
[Clock](./doc/sensor/clock.md) | ```sensors/clock```  | Vehicle | Vehicle, Ruter Sales
[Apc sensors](./doc/sensor/apc-sensors.md) | ```ruter/{PTO}/{vehicleID}/sensors/apc_sensors```  | Vehicle | Ruter Bo
[Telemetry](./doc/sensor/telemetry.md) | ```ruter/{PTO}/{vehicleID}/sensors/telemetry```  | Vehicle | Ruter Bo

 --- 

