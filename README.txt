This is a library for a Monochrome OLEDs based on SH1106 drivers

These displays use SPI to communicate, 4 or 5 pins are required to  
interface

This library is a fork of the Adafruit_SSD1306 library and modified to work with the
SH1106 driver.
Differences between the SSD1306 and SH1106 seems to be:

1) The OLED I purchased only seems to support PAGE memory mode.  I Tried the HORIZONTAL memory mode used by the SSD1306 Adafruit library and eventhough the SH1106 datasheet says it should work I had no luck.  No matter what I did.
2) The hardware scrolling does not work.  I followed the datasheet with no luck.
3) The memory buffer is actually 132x64 and the OLED view is centered on this.  This means what you see at 0,0 pixel is actually 2,0.  The 128x64 buffer is written at SEG2 (pixel 2) to compensate.

All kudos to Adafruit and Limor Fried/Ladyada for this library and making this port a pleasure.

To download. click the DOWNLOADS button in the top right corner, rename the uncompressed folder SH1106. Check that the SH1106 folder contains SH1106.cpp and SH1106.h

Place the SH1106 library folder your <arduinosketchfolder>/libraries/ folder. You may need to create the libraries subfolder if its your first library. Restart the IDE.

You will also have to download the Adafruit GFX Graphics core which does all the circles, text, rectangles, etc. You can get it from
https://github.com/adafruit/Adafruit-GFX-Library
and download/install that library as well 

/**************************************************************************************************/
This is a library for our Monochrome OLEDs based on SSD1306 drivers

  Pick one up today in the adafruit shop!
  ------> http://www.adafruit.com/category/63_98

These displays use SPI to communicate, 4 or 5 pins are required to  
interface

Adafruit invests time and resources providing this open source code, 
please support Adafruit and open-source hardware by purchasing 
products from Adafruit!

Written by Limor Fried/Ladyada  for Adafruit Industries.  
Scrolling code contributed by Michael Gregg
BSD license, check license.txt for more information
