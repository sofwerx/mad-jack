Logging is a key component of the Safe House project. This page will outline the steps to log smart device communication for use in the ELK stack.

As mentioned in the device overview, a big issue to address was compatibility between the smart devices. Conceptually, this seems simple, but nowadays, a good chunk of consumer IoT devices use cloud services to essentially lock functionality. A few attempts were made to unlock these devices with little results. The alternative we went for involved using IFTTT.com. It's a popular web service for automating tasks, and has partnered with many other services and vendors to extend support.

We're going to use IFTTT.com to report and send notifications on the status of our safe house devices to web listeners. These are web servers, run from Docker containers, that receive notifications from IFTTT and formats the data for use in Elasticsearch.



## Domoticz Data Push
Through its JSON API, Domoticz supports notification of device state. An HTTP listener was established to take data sent from Domoticz and parse the information into Logstash, which can then be indexed into Elasticsearch.

### Build and run Domoticz Web Listener

### Configure Domoticz Notifications

## IFTTT
To enable notifications to the ELK stack, you will need to make use of the IFTTT.com web service.
### Account Connection
1. Register for a free account at IFTTT.com
2. On the web UI, click **Services** and search for Smart Life. You will be prompted to enter your Smart Life credentials to connect your Smart Life account to IFTTT.

### IFTTT to Domoticz
