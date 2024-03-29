# Changes in API v2.1
## Intro
The intro section of the documentation has been altered
## Operational Information
### Assignment Attempt
- Added documentation
- Made `fromDateTime` optional

##Proprietary Extensions
### Sales and Validation
#### Deprecation
`ruter/{PTO}/{vehicleID}/pe/sales_validation`

This topic will be deprecated from future versions, it is recommended to use sales, validation and Sales: Diagnostics

### Sales Diagnostics
#### New Topic
`ruter/{PTO}/{vehicleID}/pe/sales/diagnostics`

Health status for the Sales application "Ruter Salg" and it peripheral connections. Diagnostics performed and reuslts sent before every stop.
### Sales Result
#### New Topic
`ruter/{PTO}/{vehicleID}/pe/sales/saleresult`

Sale result message generated by RuterSalg after each ticket order. This topic is intended as a live view of sales for health monitoring performance insight purposes. Must not be used for accounting, settlement or other financial calculations.
### Sales Validation
#### New Topic
`ruter/{PTO}/{vehicleID}/pe/sales/validationresult`

Validation result message generated by RuterSalg after validation of Travel card ticket. This topic is intended as a live view of validation count and results.

### DPI Extentions
#### New Topics
`{PTO}/ruter/{vehicleID}/pe/dpi/#`
`ruter/{PTO}/{vehicleID}/pe/dpi/#`

It is in Ruters interest to provide a rich and dynamic personal user experience onboard our vehicles. To provide flexibility these two topics and corresponding subtopics must be bridged between Ruter BO and the vehicle. Data will be produced and consumed only by Ruters systems.

No payload structure is defined.

### Door Locks
#### New Topics

### Active Cab
#### New Topic
`ruter/{PTO}/{vehicleID}/pe/activecab`

Tram Only

Used to keep track of what direction the train is driving


### Sensor

#### Stop Button

Added field `messageNumber`

#### Odometer

Added field `messageNumber`

#### Telemetry

- Added field `messageNumber`.
- `{sensorID}` is now specified as part of the topic name.

#### APC Sensors

- Added field `messageNumber`.
- `{sensorID}` is now specified as part of the topic name.


#### Location
- Altered description∫
- Added field `messageNumber`

### Operational Information
#### Current Block
Altered Description
#### Vehicle Journey Details
Altered Description
- Field `FetcherConnections` changed to `fetcherConnections`
- Field `FeederConnections` changed to `feederConnections`
- Field `Code`changed to `code`
#### Current Destination Display
- Field `text` changed to `name`

#### Expected call
Field `Code`changed to `code`
### Extended Information
#### Audio Message
Altered description

## Extended Information
### Due Information
- Removed expected_call from MQTT-topic
### Transfer Information
- Removed expected_call from MQTT-topic
