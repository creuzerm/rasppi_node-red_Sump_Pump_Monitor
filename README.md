rasppi_node-red_Sump_Pump_Monitor
=================================

Monitor for sump pump based on Node-Red running on a RaspberryPi

This is here on GitHub because I got tired of the power going out, corrupting my SD card and I need to rebuild this. Maybe you will find it useful for inspiration?
A build log on my blog http://mike.creuzer.com/2018/02/sump-pump-aquaponics-aquarium-water-level-monitoring.html 

# About

The sump-pump is one of those things that you don't pay attention to, expecting it to work - which it will, until it doesn't.

This is a simple tool to provide an announcement when the sump pump starts cycling.

It also provides some ambient sensors that can be used to better understand the heating & cooling charactoristics of a dwelling.



# Flows
There are three flows to control various aspects of the monitoring.
### Sump
Controls the data collection and presentation.

![Sump Pump Flow](https://user-images.githubusercontent.com/779440/50488705-5f181100-09c9-11e9-8a3c-aa6b93d36368.png)
### Computer
Remote monitoring of the RaspberryPi and some basic controls such as package updates and reboot. This section isn't my design, my notes don't say where they came from though - a Node-Red solution somewhere.
![Computer control Node Red Flow](https://user-images.githubusercontent.com/779440/50499592-6e6e7d00-0a10-11e9-9969-23dfe816dd13.png)

### Backup
Sends data to Dropbox for off-site storage. This is also maintained as a Node-Red 'Project' and changes are pushed here to github.
![Dropbox controls Node Red Flow](https://user-images.githubusercontent.com/779440/50499583-5565cc00-0a10-11e9-9ccb-02aca851c234.png)





# Sensors
This uses a pair of bmp280 temperature / pressure sensors. One of these is attached to the raspberry pi and the other is put in a PVC Pipe. The PVC pipe is capped and sealed on one end, which holds the sensor, and the other end is placed down into the sump, resting on the bottom. When water enters the sump, it compresses the air in the PVC tube, increasing the pressure and is easy to read.

The only required sensor is the one in the PVC tube, the other one was used as a reference to determine what a sump cycle actually looks like.

![Raspberry Pi on sump pump](https://pbs.twimg.com/media/DvDPZ_8VAAAld-1.jpg:large)

Here you can see a RaspberryPi Zero W powered off a automotive USB/12v socket wired to the deep cycle battery. The sensor by my thumb is a BMP280 wired to the alternative ID. Following the cat5 wire down you can see the white PVC pipe with the other sensor in the cap at top.