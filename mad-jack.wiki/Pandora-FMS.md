Pandora FMS was used in the Mad Jack's Range as a monitoring tool. Pandora FMS is an open-source software that can monitor a network -- routers, switches, and other wired or wireles connected devices. When monitoring a network, the Console (a user-friendly visual aide) can identify devices via auto-detect and name each by its IP address. 
The Console can be viewed on-site (connected to the network it is monitoring) and remotely. Also, an devices – also known as Agents – can be viewed remotely from the Console. 

Figure 1 is a view of a device where a Agent software was pre-installed (as opposed to the device found on the network via auto-detect). Installing the Agent software onto a device will allow the Console to view more information like the device’s uptime (in seconds) or the current battery level. These identifiers are known as the device’s Modules.

To view this agent the controls are on the left toolbar: Agent > Views > Agent Detail. 

## Installing Pandora FMS Agent on an Android Device

##### The devices used at the Range are Google Pixel XL, Android Software Version 8.1.0.

To install Pandroid: Pandora FMS Agent, access the Google Play Store > Search “Pandroid” > Install.

When installing the Pandora Agent onto a cellular device, it will be found in the Google Play Store under Pandroid. The first figure labeled “status” demonstrates several details such as positional data, device up time, and battery level. On the next screen labeled “setup,” the Server Address, Port, and Interval are necessary to reach the Pandora Servers to report back to the Console.

As noted in Figure 3 and 4, there are two tabs that will require user input. 

#### Setup

Server Address: The Server Address is necessary to export the data from the device. This will be found from the setup with the Pandora FMS Server and Console.

Server Port: “41121” is the default port. This is the Pandora FMS Server where the information is sent.

Interval: The default interval is 300 (seconds). This is the time when the module exports the device’s information to the Pandora FMS Server. 

Agent Name: This is the name of the device labeled in Pandora FMS Console.

XML Buffer Size: This is default 256 and required only for the Enterprise Edition.

Mobile Server URL: This is default <hostname>/pandora_console/mobile.

**Note: Pandroid will ask on initialization if the Systems Administrator would like to setup a password. This is necessary if you wish to regulate the data reported to Pandora FMS Server and Console.**

## Installing Pandora FMS Agent on Linux Workstation

The System requirements for each Linux Machine will differ depending on OS.
##### The Range used System76 Linux Workstations with Pop_OS 17.10 64-bit.

Step 1: Go to https://sourceforge.net/projects/pandora/files/Pandora%20FMS%207.0NG/721/Debian_Ubuntu/ 

Step 2: Install Pandora FMS Agent

Step 3: Click "Keep"

Step 4: Install the Agent through __Eddy__.

Step 5: Find the File ```pandora_agent.conf``` The Range directory for this file is ```home/etc/pandora```

$ cd home/etc/pandora/
$ sudo vi pandora_agent.conf

When you enter the vim editor for pandora_agent.conf, there are a few formatting edits that need to be completed to connect to your Pandora FMS server. On workstation rangecontrol0, the server_ip needs to be inserted and the rand_name line needs to be deleted.

With the blinking cursor, you should scroll down to ```server_ip``` and type ```i```. This will turn the cursor into edit mode. The Range's Pandora FMS Server connects to ```console.brangepandora.devwerx.org```

Press <esc> to exit insert mode.

Scroll down further to:
```If set to __ rand __ the agent will generate a random name``` delete (```d```) the line ```rand_name```. The correct formatting should look like this.

Press <esc> to exit delete mode.

To exit the vim editor, type ```:wq!``` and <enter> and it will return you to the command line.

Step 6: Next, you must enable the daemon to star the Pandora FMS agent. In the same folder, ```home/etc/pandora, type this command: 

$ sudo systemctl start pandora_agent_daemon.service
$ sudo systemctl enable pandora_agent_daemon.service
$ sudo systemctl status pandora_agent_daemon.service.

Step 7: The final command to verify a working Pandora FMS agent: 

$ sudo tail -f /var/log/pandora/pandora_agent.log

Conclusion: When completing these commands, the computer will now be conneccted to the Pandora FMS Server and you should be able to view the Agent Details in the Pandora FMS Console.
