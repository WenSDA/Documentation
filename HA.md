# Home Assistant

Home Assistant is what controls the majority of the systems at the church. Home Assistant is an open source home-automation solution and can be found [here](https://www.home-assistant.io/).
Home Assistant runs on a Raspberry Pi 4b in the Network and Electrical Room accessed from the backstage hallway.
Home Assistant can be accessed by navigating to [ha.wenatcheeadventist.org](https://ha.wenatcheeadventist.org)

```
HA URL: ha.wenatcheeadventist.org
HA IP: 10.0.1.3
HA WebGUI Port: 8123
HA MAC:
```

## Smart Plugs

HA controls smart plugs around the church, including spot lights, audio equipment, and Christmas lights during Christmas.
Most of these smart plugs are fiet electric. These fiet electric smart plugs are based on the Tuya framework. HA controls them via the Local Tuya repository within [HACS](HACS.md).
The two for either side of the sanctuary's spotlights are Kauf smartplugs and can be found on [Amazon](https://www.amazon.com/KAUF-Monitoring-ESPHome-Compatible-Assistant/dp/B0BJLGNPPX?th=1) or on their [GitHub Repo](https://github.com/KaufHA/PLF12).

## Nginx Proxy Manager

HA has a number of add-ons to allow for more functionality. One of which is Nginx Proxy Manager.
The router is configured to forward any traffic from the WAN interface on ports 80 and 443 to the home assistant IP address 10.0.1.3. Nginx, who is configured to take ports 80 and 443, gets that traffic and is able to proxy it to another location, acting as a middle man. (Check the [DNS documentation](DNS.md) for more information on that)
This means that you can go to ha.wenatcheeadventist.org, and that traffic goes to the router, to HA, to Nginx Proxy Manager, and Nginx Proxy Manager is configured to forward it back to HA at port 8123, opening the HA web interface.
Its also configured to proxy nginx.wenatcheeadventist.org to 10.0.1.3:81, which is the IP and Port of the Nginx Proxy Manager add-on. This gives authorized users access to the Nginx Proxy Manager Web GUI where they can configure the proxy hosts, SSL information, and other functions.

The HTTPS SSL certifacates come from Let's Encrypt under the email address wensdamedia@gmail.com.

## [DMX Spotlights](Stage-Lights.md)

Home Assistant is configured to control the stage spotlights and the [AC houselights](Houselights.md) via DMX. A "hack" within [HACS](HACS.md) allows data to be sent using the ArtNet protocall to a set IP Address. With this, DMX lights show up as regular HA lights in the HA dashboard. These lights can then be controlled by automations within HA, including control by the [buttons and button panels](HA-Button-Panels.md) around the church, as well as [ProPresenter](ProPresenter.md). Home Assistant allows for endless possibilties with our lighting.

## [Up Lights](Up-Lights.md)

Three Tuya Uplights are on the back of the stage. These are plugged into power at the left side of the stage. They connect to the IOT wifi and connect to HA with the Local Toya repository within [HACS](HACS.md).


