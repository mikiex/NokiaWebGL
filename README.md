IMPORTANT NOTE: Nokia Maps no longer exists, so this project is obsolete.

Nokia 3D WebGL Maps
===================

This is me experimenting with extraction of 3D data from the Nokia tiles.

``tiles.py`` requires Modest Maps (``pip install ModestMaps``), otherwise it
uses only the Python 2.6 standard library. To choose a different tile, scroll
all the way to the bottom and edit the latitude, longitude, and zoom. At the
moment, I'm stuck with the height lookup tables, getting correct height values
for Oakland but too-small values for San Francisco.

Changes by Mikiex
=================
Outputs multiple tiles, you specify X and Y amount in the Tiles.py file (example is 8x8)
outputs OBJ Mtl file, so JPEGS are imported with OBJ (Tested in 3ds Max import)
Issues:
All tiles are at origin 0,0,0 (so need moving in 3D app)
Some tiles may be duplicated because position of the next tile is a fixed value.

#Note possibly this and the original requied PIL to be installed.

Sample usage:

    python tiles.py

Output:

 #   out_XY_0_0_Object_0.obj
 #  out_XY_0_0_Object_0.mtl
 #	out_XY_0_0_Object_0.jpg
 #	out_XY_0_1_Object_0.obj
 #   out_XY_0_1_Object_0.mtl
 #	out_XY_0_1_Object_0.jpg
 #	etc

![Sample blender image](https://raw.github.com/migurski/NokiaWebGL/master/sf-ovi-blender.gif)
