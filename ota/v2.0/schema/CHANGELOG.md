# Changes in API v2.0
## Driver Interaction
### Assignment Attempt Rejection
- Change first `Result` to `result`
- Change second Result to errorText
## Extended Information
### Audio Message
- Change example `eventTimestamp` to `eventDateTime`
### Transfer Information
- Change example, remove spaces in key `presentedDepartureTimes`
## Proprietary Extension
### Sales Validation
- Removed all required fields - All fields are now optional
- Example message is now valid
## Operational Information
### Unique Identifier
- Change `Value` to `value`
### Vehicle Journey Details
- Organisation Info -> Change `Number`to `number`
- Place -> Change `snortName` to `shortName`
- Example -> Remove `orientation from example, orientation is not defined in the schemas
### Expected Call
- Change `AtStop` to `atStop`
- In example, field `atStop` remove quotes around `true`
### Current Destination Display
- In Example Change `text` to `name`
