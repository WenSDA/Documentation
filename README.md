# Documentation

## [Network](Network.md)

### [Unifi Networking Systems](Unifi.md)

The router and main network infrastructure located in the Network and Electrical room is unifi equipment. A UDM Pro serves as the router, and a USW 24 PoE is the main network switch. Unifi WiFi access points connect directly to this switch and are powered by it over the ethernet connection.
The Unifi equipment can be managed by navigating to [unifi.ui.com](https://unify.ui.com).

```
Router IP:
Router LAN MAC:
Router WAN IP:
ROUTER WAN MAC:
```
```
Switch IP:
```

## [Home Assistant](HA.md)

Home Assistant is what controls the majority of the systems at the church. Home Assistant is an open source home-automation solution and can be found [here](https://www.home-assistant.io/).
Home Assistant runs on a Raspberry Pi 4b in the Network and Electrical Room accessed from the backstage hallway.
Home Assistant can be accessed by navigating to [ha.wenatcheeadventist.org](https://ha.wenatcheeadventist.org)

```
HA URL: ha.wenatcheeadventist.org
HA IP: 10.0.1.3
HA WebGUI Port: 8123
HA MAC:
```

## [HA Button Panels](HA-Button-Panels.md)

Custom button panels communicate with HA to turn on lights, sound equipment, Christmas lights, and do other things. They are ESP32 or ESP8266 powered, and are fully reprogrammable if necessary. Click [here](HA-Button-Panels.md) for more information.
