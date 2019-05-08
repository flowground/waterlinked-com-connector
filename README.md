# ![LOGO](logo.png) The Water Linked Underwater GPS **flow**ground Connector

## Description

A generated **flow**ground connector for the The Water Linked Underwater GPS API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/waterlinked.com/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:44:50+03:00

## API Description

API for the Water Linked Underwater GPS. For more details: http://www.waterlinked.com

Recommended approach for connecting to a Underwater GPS via the API is:
- If "GET /api/" times out, the Underwater GPS is not running (on this IP address)
- If "GET /api/" responds with 200 OK check that the api version returrned (eg "v1") is supported by the client (eg: also supports "v1").
- If the api version returned does not match what the client supports: give an error to the user and recommend upgrading. (Eg: response is "v2" while client only supports "v1")
- If "GET /api/" responds with 301 Moved permanently. "GET /api/v1/version" to check if the kit has a version earlier than 1.5.
- "GET /api/v1/version" will always respond with 200 OK on Underwater GPS earlier than 1.5 release.

Configuration API is is not considered stable and will potentially be changed

## Authorization

This API does not require authorization.

## Actions

### ApiVersion about

*Tags:* `about`

### Get about

> Get about information

*Tags:* `about`

### Status about

> Get current IMU and GPS status

*Tags:* `about`

### Temperature about

> Get board temperature

*Tags:* `about`

### Get config

> Get generic configuration

*Tags:* `config`

### Modify config

> Modify generic configuration

*Tags:* `config`

### ListReceiver config

> (Re)Load current receiver settings and return them

*Tags:* `config`

### ShowReceiver config

> Get receiver configuration by id

*Tags:* `config`

#### Input Parameters
* `ID` - _required_ - Identifier

### ModifyReceiver config

> Modify receiver configuration, does not apply the change until generic modify is called. Calling list will discard changes

*Tags:* `config`

#### Input Parameters
* `ID` - _required_ - Identifier

### SetDepth external

> Set depth from external source. If Locator A1 is used, this is required to get a position

*Tags:* `external`

### SetMaster external

> Set current global position of master electronics from external source. Values are only used if GPS mode is set to use external GPS

*Tags:* `external`

### GetOrientation external

> Get orientation of ROV/Locator set by external

*Tags:* `external`

### SetOrientation external

> Set orientation/compass heading of ROV/Locator. This is used only for visualization in GUI

*Tags:* `external`

### Create poi

> Create a new POI

*Tags:* `poi`

### List poi

> List all points of interest

*Tags:* `poi`

### Delete poi

*Tags:* `poi`

#### Input Parameters
* `ID` - _required_

### Show poi

> Get a POI

*Tags:* `poi`

#### Input Parameters
* `ID` - _required_

### Update poi

*Tags:* `poi`

#### Input Parameters
* `ID` - _required_

### AcousticFiltered position

> Get current Kalman filtered acoustic position relative to master acoustics. Expected update frequency: 4 Hz

*Tags:* `position`

### AcousticRaw position

> Get current unfiltered acoustic position relative to master acoustics. Expected update frequency: 4 Hz

*Tags:* `position`

### Get position

> Get current global position of locator. Locator position is calculated from the current acoustic position and the global position of the master electronics. Expected update frequency: 4 Hz

*Tags:* `position`

### GetMaster position

> Get current global position of master electronics. Expected update frequency: 1 Hz

*Tags:* `position`

### Get warnings

> Get current list of messages

*Tags:* `warnings`

## License

**flow**ground :- Telekom iPaaS / waterlinked-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
