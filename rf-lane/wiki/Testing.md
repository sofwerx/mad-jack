## HackRF/Transmitter Jamming Test
The final part of implementing the system is to test and identify the usability and preset a baseline which can be shown as an attack in an algorithm. Some tools useful for the testing process are as follows:

GNU Radio - `apt install gnuradio`

[Osmocom SDR](https://osmocom.org/projects/sdr/wiki/GrOsmoSDR)

[GQRX](http://gqrx.dk/download/install-ubuntu)

With configuration of the listed tools or any other type transmitters you can test whether introducing a replay/jamming attack among the devices being monitored properly registers.

Setting HackRF's with GQRX to watch the desired frequency and this OsmocomSDR command `sudo osmocom_siggen -a hackrf -s 2000000 -f 908420000 -g 67 --sine -x 25000` will enable you to transmit a signal at a wanted frequency and verify its effectiveness. However you should note that using a HackRF might have insufficient result in jamming due to the weaker power it emits. Verification of the attack should be made through checking the device communication and the database for proper results (lack of communication and increase in hits).

![](https://github.com/peteIS/mad-jack/blob/master/Testing.png?raw=true)

Using any testing involving transmission of signal must include integration of a Faraday cage or other shielding techniques. Otherwise depending on the frequency, transmission of signal could lead to interference with crucial public and private spectrum's which are regulated by the FCC. This could lead to tampering important systems and result in a fine. Creating any interference should be monitored closely with any sort of a spectrum analyzer like GQRX. This would provide best and quickest feedback on any signal generated and moving within the specified RF spectrum. 

![](https://github.com/peteIS/mad-jack/blob/master/GQRX.png?raw=true)