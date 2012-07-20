munin-openweather
=================

Creates Munin graphs from the data at [Open Weather Map](http://openweathermap.org/) which are extracted
via their [JSON-API](http://openweathermap.org/example-json).

Note: Against their statement "temp - Temperature in Kelvin." the temperatures are **not** in Kelvin but degree Celsius!

Install
-------

Clone this repository or download the openweather_ file and create a
symlink as *root* in /etc/munin/plugins by using e.g.:

	cd /etc/munin/plugins; ln -s /path/to/openweather_ openweather_<type>_<id>

where <type> is one of [station, weather] and <id> is a suitable station or city id.
(You can easily get the ID when you navigate to your station/city of interest and open
the detail page for this station by clicking on it - your URL should contain the id then.)

**Don't forget to restart your munin-node deamon.**
