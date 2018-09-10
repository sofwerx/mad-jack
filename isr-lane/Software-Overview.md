A goal for this project is to make as much use of open-source software as possible. While some proprietary applications and services proved necessary, a closer examination of equipment options could reduce the need for non-free software. Here are the applications and services used in the Safe House project. During the project, some of these applications run off a Docker container. This is not absolutely essential, but greatly facilitates software deployment.

## Domoticz
![](https://www.thermosmart.com/wp-content/uploads/2015/09/domoticz.png)

Domoticz is a free and open source home automation manager available on Windows, MacOS, and Linux platforms as well as for several embedded devices. It supports the integration of a wide variety of technologies, including Z-Wave, Zigbee, RFXCOM, Smart Meter, and more. Additionally, Domoticz's API allows for device communication with JSON, so if a device can be configured to communicate over the local network via JSON, it can be integrated into a Domoticz system as well. Domoticz features native support for log exports to InfluxDB, Google PubSub, FibaroLink, or via HTTP. Notifications may also be sent in JSON to a web listener. In the safe house project, Domoticz was deployed in a Docker container.
For a partial list of devices compatible with Domoticz, please refer to the Domoticz wiki here:
* https://www.domoticz.com/wiki/Hardware

Apart from its documentation, Domoticz is supported by an active community of users and makers: providing an additional source of troubleshooting assistance as well as feature extensions with user-contributed scripts.
* **Download:** http://www.domoticz.com/downloads/
* **Documentation:** https://www.domoticz.com/wiki/Main_Page

## August Home
![](https://is2-ssl.mzstatic.com/image/thumb/Purple128/v4/9a/24/25/9a2425b5-fa01-5e3d-3822-c775f8d5dded/AppIcon-1x_U007emarketing-0-0-GLES2_U002c0-512MB-sRGB-0-0-0-85-220-0-0-0-3.png/246x0w.jpg)

This is a proprietary smart phone app, for iOS and Android, that the manufacturer requires for operation of their August Smart Lock. The application needs internet access for account registration. After your account has been authenticated and hardware has been linked to your account, the user may control the lock using Bluetooth. The application uses AES-encryption for authentication. The application also authorizes guest access to the lock, displays the logs of lock activity, and adds other August devices, such as the Connect hub, for use in their system.

* **Google Play**: https://play.google.com/store/apps/details?id=com.august.luna
* **iOS App Store**: https://itunes.apple.com/us/app/august-home/id648730592?mt=8

## Tuya Smart Life
![](https://lh3.googleusercontent.com/7j5Lom_UrwVEvpq3OKVFkR24U4OYWulp0DIDg6jrJtl9ybA3Fh-E1xl7cyooouTG0YE=s180)

This is a proprietary smart phone application, for iOS and Android, that the manufacturer requires for operation of their Wi-Fi devices. These include Wi-Fi power plugs and Wi-Fi smart lights. The application needs internet access for account registration, and then access to the same local area network as the Wi-Fi devices for operation. Tuya claims it protects its applications with "military-grade" encryption.

* **Google Play:** https://itunes.apple.com/us/app/smart-life-smart-living/id1115101477?mt=8
* **iOS App Store:** https://itunes.apple.com/us/app/tuyasmart/id1034649547?mt=8

## IFTTT
![](https://aem.dropbox.com/cms/content/dam/dropbox/www/en-us/business/app-integrations/ifttt/ifttt-logo.png)

IFTTT (If This Then That) is a web service that provides a platform for inter-connectivity and automation between a wide variety of disparate web services and IoT devices. IFTTT enables automation through the use of a series of conditional statements via a very user-friendly web interface. These statements are based on triggers provided by IFTTT partner vendors and manufacturers. IFTTT is proprietary. Although it supports a large swathe of popular devices and services, IFTTT requires an internet connection. In addition to basic triggers, IFTTT also provides a means to send JSON data to a user-provided public address. Security-wise, the user may elect TLS for this communication.


## Amazon Alexa
![](https://upload.wikimedia.org/wikipedia/en/9/9e/Amazon_Alexa_Logo.png)

Amazon Alexa is a popular virtual assistant providing voice-activated functionality to a variety of services and devices. It requires the user to register for a free Amazon account for use. It runs off of Amazon's Echo devices and needs internet access. Alexa support is provided by most newer IoT devices.

## Elasticsearch
![](https://www.elastic.co/assets/blt6050efb80ceabd47/elastic-logo%20(2).svg)

Elasticsearch is a powerful, cross-platform, free and open source search engine used to query documents in near real time. It's based off the earlier Lucene search engine and is one of the most popular open source search engine and is used by many tech companies, namely Facebook, Adobe, Netflix, and Github. It's operated from an HTTP web interface. In the safe house project, Elasticsearch was deployed in a Docker container.
* **Download:** https://www.elastic.co/downloads/elasticsearch
* **Documentation:** https://www.elastic.co/guide/index.html

## Kibana
![](https://s3-ap-south-1.amazonaws.com/av-blog-media/wp-content/uploads/2017/05/15033303/csm_Kibana-Logo-Color-H_4bc61d6148.png)

Kibana is a data visualization plugin for Elasticsearch. It's commonly deployed as part of an ELK stack: Elasticsearch, Logstash (for document parsing), and Kibana. Kibana provides several dashboards for creating pie charts, histograms, or line graphs. Its API also allows for creation of custom data visualizations. It reports in near real time, and includes tools for monitoring and notifying on incoming data. In our setup, Kibana is run from a Docker container.
* **Download:** https://www.elastic.co/downloads/kibana
* **Documentation:** https://www.elastic.co/guide/en/kibana/current/index.html
