Motivation
==========

You may be familar with the `Web Mercator`_ (or Spherical Mercator, Google Tiles, etc) tiling scheme, which is the most commonly encountered tiling scheme on the web.  There are good tools out there for dealing specifically with this projection, for instance Mercantile_ fits the bill.  If you're dealing exclusively with this projection, you might get better mileage with them!

One oddity of Web Mercator is that coordinates are usually expressed in geographic (longitude, latitude) coordinates that live on the ellipsoid (WGS84) rather than in units of the Web Mercator projection (meters).  Dealing with this kind of conversion is exactly what Mercantile_ and its like were made to handle.

Tiletanic's use cases are a bit different:

- What do you do if your data is already in some projection?  For instance, you might want to know what tile covers a point specified in the Web Mercator projection without first converting back to WGS84.  Tiletanic can help.
- At DigitalGlobe_, our imagery is often projected into many other projections (UTM, Geographic, etc) and it is often times extremely convienent to organize raster data into a tiled format before proceeding with processing (a single "strip" from one of our satellite collects can easily be 100km long!).  When dealing with different projections, the user typically needs to impose their own tiling scheme.  Tiletanic provides an easy way for you to define you're own scheme and get a lot of tiling functionality right out of the gate.

.. _`Web Mercator`: https://en.wikipedia.org/wiki/Web_Mercator
.. _Mercantile: https://github.com/mapbox/mercantile
.. _DigitalGlobe: https://www.digitalglobe.com/
