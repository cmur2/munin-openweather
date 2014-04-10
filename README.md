munin-openweather
=================

Creates Munin graphs from the data at [Open Weather Map](http://openweathermap.org/) which are extracted
via their [JSON-API](http://openweathermap.org/wiki/API/JSON_API) (Version 2.5).

Temperatures are now given in Kelvin and this plugin uses an offset of 273.15 to convert to degree Celsius.

Upgrading
---------

If you're using version [115fb0875f](https://github.com/cmur2/munin-openweather/commit/115fb0875f41dc6e493963ca0cbfe2700c31c2ad)
or prior you might consider renaming your symlinks from <type> "weather" to "city" - by default the script
will do rename internally for compatibility reasons (SYMLINK_COMPAT flag true).

Install
-------

Clone this repository or download the openweather_ file and create a
symlink as *root* in /etc/munin/plugins by using e.g.:

	cd /etc/munin/plugins; ln -s /path/to/openweather_ openweather_<type>_<id>

where <type> is currently ignored (formerly one of [station, weather]) and <id>
is a suitable city id.
(You can easily get the ID when you navigate to your station/city of interest and open
the detail page for this station by clicking on it - your URL should contain the id then.)

**Don't forget to restart your munin-node deamon.**

License
-------

[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
