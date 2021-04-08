# API v. 2.1 [Draft]
> DISCLAIMER: This document is in it’s current form regarded as a draft. It will be finalized before the end of January 2021

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
