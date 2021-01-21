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
