# AHT20-raspberry-pi

Read AHT20 sensor using Raspberry Pi. Publish in a format suitable for my HomeAssistant setup. Typical output would look like

```text
 {"t": 1711595102, "temp": 71.0, "humid": 36.4, "device":"AHT20"}
```

Where `t` is the seconds since the start of the epoch, `temp` is temperature in °F and `humid` is relative humidity in %. `device` identifies the device used. There may be additional fields for debugging information and yes, this is JSON. It will be wriotten to STDOUT and in operation, piped ti `mosquitto_pub` which will add a suitable topic and publish to a designated MQTT broker.

## Motivation

Try yet another temp/humidity sensor

## Plan 

Copy the project from `.../aht20/project/raspberrypi4b/` found in <https://github.com/HankB/aht20/> which provides the library used. This project adopts the MIT License used in that project.

## Requirements

See [original requirements](./raspberrypi4b/README.md#21-dependencies)
ls -l

## Progress/status

No joy. The application uses too many things in other parts of the original project. Instead of separating things, I will return to (my fork of) the original project and create a branch in which I can modify the applications to meet my needs.

At present this effort is on hold. See <https://github.com/HankB/aht20> for further progress.
