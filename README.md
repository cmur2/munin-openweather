munin-openweather
=================

Creates Munin graphs from the data at [Open Weather Map](http://openweathermap.org/) which are extracted
via their [JSON-API](http://openweathermap.org/wiki/API/JSON_API) (Version 2.0).

Temperatures are now given in Kelvin and this plugin uses an offset of 273.15 to convert to degree Celsius.

Upgrading
---------

If you're using a version prios to [this one](https://github.com/cmur2/munin-openweather/commit/115fb0875f41dc6e493963ca0cbfe2700c31c2ad)
you have to rename your symlinks of <type> "weather" to "city".

Install
-------

Clone this repository or download the openweather_ file and create a
symlink as *root* in /etc/munin/plugins by using e.g.:

	cd /etc/munin/plugins; ln -s /path/to/openweather_ openweather_<type>_<id>

where <type> is one of [station, city] and <id> is a suitable station or city id.
(You can easily get the ID when you navigate to your station/city of interest and open
the detail page for this station by clicking on it - your URL should contain the id then.)

**Don't forget to restart your munin-node deamon.**
