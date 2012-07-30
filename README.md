worldMap.js
===========

Draw world map on canvas

##Inroduction

Spent quite some time searching on web on converting latitude/longitude to pixel. Pretty common question I thought. Amazingly, no simple answer. Everybody wanted to write either a academic paper, or a gmap tutorial.

WTF, I just wanted to draw a small world map and plot some stuff on top! What projection? Well, the one that commonly used by 3rd party ip to lat/lon translation.

Until somebody mentioned, for small size map, lat/lon are quite linear...

So, here is the magic formula:

    var x = ((lng / 360) + 0.5) * width;
    var y = (1 - ((lat / 180) + 0.5)) * height;

Then get lands shapfile from [Natural Earth](http://www.naturalearthdata.com/). Extract out lat/lon by using [shpdump](http://shapelib.maptools.org/shapelib-tools.html#shpdump). We got a map.

##Screenshot

![demo](https://github.com/richardzcode/worldMap.js/blob/master/worldMapDemo.png?raw=true)
