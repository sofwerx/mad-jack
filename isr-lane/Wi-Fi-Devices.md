Incorporating Wi-Fi devices into the safe house system will require the use of non-free software and services, as well as constant connection to the Internet. Ensure your smart phone is connected to the Internet.

## Smart Bulb
1. Connect the bulb to a light socket. Proceed to turn the bulb on, then off, 10 times to enable device discovery. The bulb will begin flashing to confirm discovery mode.
2. On a smartphone connected to the safe house's Wi-Fi network, run the **Smart Life** application. Register for a free account if you haven't already.
   * [iOS](https://itunes.apple.com/us/app/smart-life-smart-living/id1115101477?mt=8)
   * [Android](https://play.google.com/store/apps/details?id=com.tuya.smartlife&hl=en_US)
4. From your home screen, tap the **Add Devices**. Choose **Lighting Devices** on the next screen.
5. Confirm the rapidly flashing light on the app. The app will now search your network. Complete setup within the application.

## Smart Plugs
The plugs use the same application as the bulb. Connect the plug to a socket and press the power button on the front of the plug to enable discovery, and follow the same instructions as in the previous section, choosing **Smart Plug** as device type.

## Amazon Alexa and Google Home.
A quick comparison between Amazon Alexa and Google Home will show that a greater number of devices support Alexa over Google Home. In the case where a device supports both services, it's usual that more functionality is provided by Amazon Alexa than the Google smart assistant. For adding voice activation to the smart home, we mostly relied on Amazon Alexa because it provided more functional triggers on the IFTTT service, which is important for monitoring purposes. However, the two smart assistants are very similar when it comes to setting them up, so feel free to use Google Home in addition to Alexa.

Setup of these smart assistants must also be done through a smart phone app. Power the Amazon Echo Dot and Google Home Mini, and install their respective apps on your phone. If you do not already have an Amazon (or Google) account, you will be prompted to create one.
* [Google Home - iOS](https://itunes.apple.com/us/app/google-home/id680819774?mt=8)
* [Google Home - Android](https://play.google.com/store/apps/details?id=com.google.android.apps.chromecast.app)
* [Amazon Alexa - iOS](https://itunes.apple.com/us/app/amazon-alexa/id944011620?mt=8)
* [Amazon Alexa - Android](https://play.google.com/store/apps/details?id=com.amazon.dee.app&hl=en_US)

These apps will guide you through configuration of the smart assistants on your network.

Voice connectivity is enabled by linking your smart assistant account to that of your other devices, ie August or Smart Life. In the Alexa app, you can do this by:
1. Tap the hamburger icon in the top left, and select **Skills** from the slide-in menu on the left.
2. Search for your desired skill. You will need to do these steps for the **Smart Life** and **August** skills.
3. Tap **Enable Skill** and the app will walk you through linking your Amazon account with the 3rd party service. You will be prompted for your account credentials as well as permissions.
4. When completed, you should be able to control your devices from the Alexa app. Check the Skill in the Alexa menu to see available functions. Most are intuitive, such as "Alexa, turn on the light."

## VStarCam Wi-Fi Camera
If you haven't noticed a trend in the devices we've been using, they're all configured from a smart phone. The camera is no exception, but thankfully we can access its functions remotely from a PC after its initial setup.
1. Hook the camera up to power; it will automatically power on.
2. Download the Eye4 app for your smart device.
    * [Android](https://play.google.com/store/apps/details?id=vstc.vscam.client&hl=en_US)
    * [iOS](https://itunes.apple.com/us/app/eye4/id642266858?mt=8)
3. Register for a new account.
4. Once registered, tap the **+** icon on the top right of your home screen. You will be conveniently presented with a QR code. Tap it to expand, and present it to the camera's lens. The LED on the camera will start flashing. The QR code contains the Wi-Fi SSID and passkey stored internally on the phone.
5. Give the camera a few minutes to complete connection to the network. Once finished, you will be prompted to finish setup on the Eye4 app, and will then be able to access its video feed. You may change the default login password, which is **admin:888888**, or you may change it as you see fit.
6. The video feed, as well as camera controls and settings, can be accessed by entering the camera's IP address and port number in a web browser or video player like VLC. However, this can be a little tedious to find since the camera assigns a seemingly random port number for this purpose. You could use something like NMap or tcpdump to try to find it, but VStarCam also provides a desktop application (not advertised in the product packaging, mind) for this very purpose. On separate machine (or VM) running Windows or MacOS, download, unzip and run the IP Camera Finder tool.
   * [Windows](http://download2.eye4.cn/download2/application/app-find-vstarcam.zip)
   * [MacOS](http://download2.eye4.cn/download2/application/app-Find-T-Mac.zip)
7. Click **Find** in the bottom of the window, and the tool will search the network for your camera, and display the available port number to access its web UI. Use this full URL to access the camera. You will be prompted for a user name and password. Again, the default is **admin:888888**
8. To access the videostream, open a video player with network streaming capabilities such as VLC, and enter the following when prompted for a URL:
`rtsp://username:password@camera.ip.address:/udp/av0_0`.
Here's an example:



The next step will involve bringing everything together for data gathering.
