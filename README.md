rasppi_node-red_Sump_Pump_Monitor
=================================

Monitor for sump pump based on Node-Red running on a RaspberryPi

This is here on GitHub because I got tired of the power going out, corrupting my SD card and I need to rebuild this. Maybe you will find it useful for inspiration?

### About

The sump-pump is one of those things that you don't pay attention to, expecting it to work - which it will, until it doesn't.

This is a simple tool to provide an announcement when the sump pump starts cycling.

It also provides some ambient sensors that can be used to better understand the heating & cooling charactoristics of a dwelling.

#### Sensors
This uses a pair of bmp280 temperature / pressure sensors. One of these is attached to the raspberry pi and the other is put in a PVC Pipe. The PVC pipe is capped and sealed on one end, which holds the sensor, and the other end is placed down into the sump, resting on the bottom. When water enters the sump, it compresses the air in the PVC tube, increasing the pressure and is easy to read.

The only required sensor is the one in the PVC tube, the other one was used as a reference to determine what a sump cycle actually looks like.

![Raspberry Pi on sump pump](https://pbs.twimg.com/media/DvDPZ_8VAAAld-1.jpg:large)