# Welcome to Brumap

Brumap is based on [MapBBCode](https://github.com/mapbbcode/mapbbcode), I'll use it by interest and to learn github. Sorry for mistakes, let's customized it for my purpose. 

## Installation

In order to reduce load on the main [share.mapbbcode.org](http://share.mapbbcode.org) website, cloning the service is encouraged. Requirements are few:

* Apache with mod_rewrite or nginx with php-fpm
* PHP 5.2 or newer
* MySQL 5
* A separate domain (or subdomain) name

To install, copy all files (except `README.md`) to a designated directory, modify `config.php` according to your setup, and open `http://domain.name/initdb`. If you see a map with a yellow message saying tables were created, you're good to go. Set `NEED_INIT_DB` in the config to `false`, then check that saving and signing in work.

For caching to work, you need a `cache` directory with writing rights.

## Formats (to be modified)

At the moment MapBBCode Share can import 11 file types and export 10. Writing a plugin for a new file format is easy: see examples in `formats` directory. Those are loaded automatically, you won't have to modify other scripts. Keep in mind this is not a universal convertor: [GPSBabel](http://www.gpsbabel.org/) is. This is not a GPS trace storage, and traces are simplified: we already have [GPSies](http://www.gpsies.com/) for full GPX downloads, elevation and speed profiles. MapBBCode Share goals are simple and outlined in the first section, and supported formats list should be kept short.

## Included Libraries

Writing the service would be much harder it it weren't for those libraries:

* [MapBBCode](https://github.com/mapbbcode/mapbbcode) (WTFPL)
* [Leaflet](http://leafletjs.com/) (BSD 2-clause)
* [Leaflet.draw](https://github.com/Leaflet/Leaflet.draw) (MIT)
* [Bing.js](https://github.com/shramov/leaflet-plugins/blob/master/layer/tile/Bing.js) (BSD 2-clause)
* [LightOpenID](http://code.google.com/p/lightopenid/) (MIT)
* [OpenID Selector](http://code.google.com/p/openid-selector/) (BSD 3-clause)
* [Simplify.js](http://mourner.github.io/simplify-js/) (BSD 2-clause)
* [Simplify.php](https://github.com/AKeN/simplify-php) (unknown license)

## License

All files that did not come from other libraries are released under [WTFPL](http://www.wtfpl.net/).
