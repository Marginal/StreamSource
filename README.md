# Live streaming software plugin for [EDMC](https://github.com/Marginal/EDMarketConnector/wiki)

This plugin outputs status info from the game [Elite Dangerous](https://www.elitedangerous.com/) to files for use as [text sources](https://obsproject.com/wiki/Sources-Guide#text-gdi) in live streaming software such as [Open Broadcaster Software](https://obsproject.com/), [GameShow](http://gameshow.net/), [XSplit](https://www.xsplit.com/), etc.

## Installation

* On EDMC's Plugins settings tab press the “Open” button. This reveals the `plugins` folder where EDMC looks for plugins.
* Download the [latest release](https://github.com/Marginal/StreamSource/releases/latest).
* Open the `.zip` archive that you downloaded and move the `StreamSource` folder contained inside into the `plugins` folder.

You will need to re-start EDMC for it to notice the new plugin.

## Output

The plugin writes the following status files into the folder that you specify in EDMC's Output settings tab:

* `EDMC System.txt` - Name or the current star system.
* `EDMC StarPos.txt` - Star system's galactic coordinates.
* `EDMC Station.txt` - Name of the planetary or space station at which the player is docked. Empty if not docked.
* `EDMC Body.txt` - Name of the nearby star, planet or ring. Empty if not near any celestial body.
* `EDMC LatLon.txt` - Latitude and longitude coordinates. Empty if not near a planet.
* `EDMC Station or Body.txt` - Name of the station if docked, otherwise the name of the nearby celestial body, or empty.
* `EDMC Station or Body or System.txt` - Name of the station if docked, otherwise the name of the nearby celestial body, otherwise the name of the star system.
* `EDMC ShipType.txt` - Ship type, e.g. Krait Phantom.
* `EDMC ShipName.txt` - Ship name, if the ship has been named. Otherwise ship type.

If the app is started while the game is not running these files hold placeholder values, which can be used to position the text in OBS Studio and other streaming software.

## License

Copyright © 2019 Jonathan Harris.

Licensed under the [GNU Public License (GPL)](http://www.gnu.org/licenses/gpl-2.0.html) version 2 or later.
