## Zwave and Motion Sensors
Depending on the signal monitored there is a variety of factors to be taken into account. Identifying the [frequency](oursera.org/browse/information-technology/security?languages=en) alone will most of the time sufficient, however understanding the activity of the protocol, activity of device communication and activity of interference are crucial in identifying a baseline of what you will be monitoring.

The protocol, or way of communication between different devices, is the one of the most complicated parts of transferring information. In the Mad Jack's Range project [Z-Wave](https://en.wikipedia.org/wiki/Z-Wave) was the monitored protocol. Due to brief communication method the type of monitoring, needed for Z-Wave, required a designated SDR which would constantly calculate the frequency activity. Other protocols like WiFi/GSM/Bluetooth have much higher data input and activity and can be averaged every several miliseconds, hence they are monitored through a wide spectrum.

Knowing the devices actively interfering/being monitored with the frequency watched helps understand where exactly and how much activity there actually is present. Through analyzing signal strength of specific devices, if stationary, they can be easily identified as a characteristic of that device. This overall will help properly organize and the infrastructure, mapping of the devices and the node that will monitor them, and identify the parameters which would separate attacks from your device communicating.

![](Zwave%20Sensor.jpg)
