# TuyAPI 🌧 🔌

[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)
[![Build Status](https://travis-ci.org/codetheweb/tuyapi.svg?branch=master)](https://travis-ci.org/codetheweb/tuyapi)
[![Coverage Status](https://coveralls.io/repos/github/codetheweb/tuyapi/badge.svg?branch=master)](https://coveralls.io/github/codetheweb/tuyapi?branch=master)

A library for communicating with devices that use the [Tuya](http://tuya.com) cloud network. These devices are branded under many different names, but if port 6668 is open on your device chances are this library will work with it.

## Installation

  `npm install codetheweb/tuyapi`

## Basic Usage

```javascript
const TuyaDevice = require('tuyapi');

let tuya = new TuyaDevice({
  id: 'xxxxxxxxxxxxxxxxxxxx',
  key: 'xxxxxxxxxxxxxxxx',
  ip: 'xxx.xxx.xxx.xxx'});

tuya.get().then(status => {
  console.log('Status:', status);

  tuya.set({set: !status}).then(result => {
    console.log('Result of setting status to ' + !status + ': ' + result);

    tuya.get().then(status => {
      console.log('New status:', status);
      return;
    });
  });
});
```

This should report the current status, set the device to the opposite of what it currently is, then report the changed status.

See the [setup instructions](docs/SETUP.md) for how to find the needed parameters.


## 📝 Notes
- Only one TCP connection can be in use with a device at once. If using this, do not have the app on your phone open.
- Some devices ship with older firmware that may not work with `tuyapi`.  If you're experiencing issues, please try updating the device's firmware in the official app.


## 📓 Docs

See the [docs](https://codetheweb.github.io/tuyapi/index.html).

## TODO

1. Document details of protocol
2. Figure out correct CRC algorithm

## Contributors

- [codetheweb](https://github.com/codetheweb)
- [blackrozes](https://github.com/blackrozes)
- [clach04](https://github.com/clach04)
- [jepsonrob](https://github.com/jepsonrob)
- [tjfontaine](https://github.com/tjfontaine)
- [NorthernMan54](https://github.com/NorthernMan54)
- [Apollon77](https://github.com/Apollon770)
- [dresende](https://github.com/dresende)

## Related

### Ports
- [python-tuya](https://github.com/clach04/python-tuya) a Python port by [clach04](https://github.com/clach04)
- [m4rcus.TuyaCore](https://github.com/Marcus-L/m4rcus.TuyaCore) a .NET port by [Marcus-L](https://github.com/Marcus-L)

### Projects built with TuyAPI
- [tuya-cli](https://github.com/TuyaAPI/cli): a CLI interface for Tuya devices
- [homebridge-tuya](https://github.com/codetheweb/homebridge-tuya-outlet): a [Homebridge](https://github.com/nfarina/homebridge) plugin for Tuya devices
- [tuyaweb](https://github.com/bmachek/tuyaweb): a web interface for controlling devices by [bmachek](https://github.com/bmachek)
- [homebridge-igenix-air-conditioner](https://github.com/ellneal/homebridge-igenix-air-conditioner): a [Homebridge](https://github.com/nfarina/homebridge) plugin for the Igenix IG9901WIFI air conditioner
- [magichome-led-controller](https://github.com/cajonKA/magichome-led-controller-node): a node to use magichome led RGB controller in [node-red](https://github.com/node-red/node-red)


To add your projects to either of the above lists, please open a pull request.

[![forthebadge](https://forthebadge.com/images/badges/made-with-javascript.svg)](https://forthebadge.com)
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)
