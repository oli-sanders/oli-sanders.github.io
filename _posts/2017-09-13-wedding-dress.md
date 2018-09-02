---
layout: post
title: DressLights
modified: 2018-08-30
---

Last year I got married to my wonderful wife and I had to bring some tech to the
wedding. So I built lights into my wife's wedding dress and on a T-shirt to wear
under my shirt. See the finished dress below.
<div class="full-width-container">
  <iframe class="video" src="https://www.youtube.com/embed/Btj4zc9LLag" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
</div>
## Parts
 * 48 [Neopixels](https://www.adafruit.com/product/1260)  36 on the dress + 12
   Neopixels on the t-shirt.
 * [Adafruit Powerboost 1000C](https://www.adafruit.com/product/2465)
 * [LIPo 2000Mah](https://www.adafruit.com/product/2011)
 * [TL-WR710N wireless router](http://uk.tp-link.com/products/details/TL-WR710N.html)  - A great portable wireless router
 * laptop
 * [Adafruit Huzzah Breakout](https://www.adafruit.com/product/2471)
 * [Arduino Pro Mini](https://www.arduino.cc/en/Main/ArduinoBoardProMini)
 * Lots of white wire & thread

## Software
The lights are controlled from a program I wrote in C#. The program plays music
from our wedding playlist and runs a beat detection algorithm which controls
when the lights change and which animation the lights are playing. The colours
the lights should be are then sent over wifi in UDP packets to the dress and the
t-shirt.

## Hardware
The Adafruit Huzzah Breakout is programmed to act as a UDP to serial bridge
sending the recieved UDP packets to the Arduino Pro Mini via serial.
The Arduino Pro Mini then converts the message into commands for the lights
which were attached to one of the digital pins of the Arduino Pro Mini.
The lights are Adafruit Neopixels soldered into 6 strings of 5 lights which were
sewed onto the dress under several layers of fabric.
Power lines were sewed in a ring around the waist of the dress, with the
Adafruit powerboost 1000C and a 2000Mah lithium polymer battery attached to the
ring.
The t-shirt had an identical setup to the dress except all 12 of the lights were
on one string.
See below for a video showing a string of lights being tested.

## Improvements that I could have made.
- The Adafruit Huzzah could have been made to control the lights as well.

## Thanks
 * My wonderful wife for sewing most of the lights on the dress and putting up
   with my techy hobbies and the piles of electronics and computer parts in our
   flat.
 * Everyone who helped and worked so hard to make our wedding day so special.
 * [Adafruit](https://www.adafruit.com)  for creating so many of the hardware
   components used in this project. I'm not affiliated with Adafruit in any way.