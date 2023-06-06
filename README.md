# Configure Charles Web Proxy on Desktops and Smartphones

Some test cycles require extended logging of the internet traffic from/to your device or a connection routed through a proxy server. For that purpose, we work with some proxy server software, such as Charles Web Proxy.

Let's go throgh the installation and configuration steps:

🔵 [Download and install Charles](https://github.com/lana-20/charles-setup/blob/main/README.md#download-and-install)

🔵 [Connect a Smartphone or Tablet to Charles](https://github.com/lana-20/charles-setup/blob/main/README.md#connect-devices)

🔵 [Capture SSL traffic using Charles](https://github.com/lana-20/charles-setup#capture-and-decrypt-ssl-traffic)

🔵 [Export device logs for attaching them to bug reports](https://github.com/lana-20/charles-setup#capture-ssl-logs)

## Download and Install

Although Charles is not an open source software or a free tool, a demo version is available. It can be downloaded and used for free, but limits each session to 30 minutes. Consequently, we have to restart the software now and then, if we want to use it for a more extended period.

<img width="600" src="https://user-images.githubusercontent.com/70295997/223296577-314ac68f-8ac3-4f2f-8ec0-aa908d9935ca.png">

Download the OS-appropriate version of [Charles Proxy](https://www.charlesproxy.com/download/).

<img width="800" src="https://user-images.githubusercontent.com/70295997/223290039-0a68dbd5-123e-4614-a880-776524a9cd54.png">

Once the installation is finished, start the software. We have to wait 10 seconds at every start.

## Connect Devices

As Charles is running now, we want to route all the network traffic from and to our devices through it. Depending on the device you plan to use, perform the following steps matching the device(s).

### Desktops

We are already done! As soon as Charles is running, it automatically captures and records all browser traffic. This procedure typically covers the most common browsers like Chrome, Firefox, Safari, and Edge. You can quickly check the proxy connection by following these steps:

♦ Ensure that **Windows** or **macOS** Proxy is enabled in the Proxy menu.
  
  ![2017-10-26_20h21_22_3](https://user-images.githubusercontent.com/70295997/223298601-12088334-9461-430a-9f3c-f3a457858bf1.gif)
  <img width="800" src="https://user-images.githubusercontent.com/70295997/223293316-92174d0f-3b47-452c-9b5e-34424a08fb9c.png">

♦ Click the 🧹 broom button (leftmost) in the Charles toolbar to clean the logs.

<img width="800" src="https://user-images.githubusercontent.com/70295997/223294009-82ac2a9a-1844-492f-9e5f-ff06417cd2f8.png">

♦ Open the browser and navigate to a random site.

♦ Observe new log entries popping up in the Charles log.

<img width="800" src="https://user-images.githubusercontent.com/70295997/223295849-98a59ccb-fec6-467a-89dd-07c9f299b1ec.png">

♦ You can also pause and resume the logging at any time using the second red/grey button in the toolbar.

<img width="600" src="https://user-images.githubusercontent.com/70295997/223294999-aef56c65-9f69-4a50-8a04-6848c91a092f.png">

If you can see yout log filling up, you are good to go.

### Mobile Devices

#### Gather ② crucial pieces of information first.

Before we can configure our mobile device to use Charles, you need to know the <code>IP address</code> of your computer (running Charles) and the <code>port</code>. This can quickly be done as follows:

♦ Click **Help > Local IP Address** to locate the IP. The address consists of four blocks of one to three digits each. In the below captioned examples, it's <code>192.168.178.100</code> or <code>10.0.0.76</code>.


♦ You also need to know the port that Charles is using. 
  
  ![2017-10-26_20h39_33](https://user-images.githubusercontent.com/70295997/223300255-ae04ed1b-f4ae-4abf-b7de-3624fd9b9edb.gif)
  <img width="600" src="https://user-images.githubusercontent.com/70295997/223618315-2daa007e-27fb-4001-b601-26319d42db06.png">
  <img width="600" src="https://user-images.githubusercontent.com/70295997/223302269-0804a6a5-bdfc-4fc0-91f7-8072fa96780f.png">

  We need both numbers for the next step.

‼️ Important note when connecting *new* mobile devices:

  Once a new device tries to connect to your Charles session, Charles will ask you to **grant the permission** to do so. Make sure to allow your connection. We also **disable or appropriately configure any firewall or internet security** and permit incoming traffic to Charles respectively to port 8888 or the port you've determined for Charles before.

#### Connect Android Smartphone

To connect an Android smartphone, head to the WiFi settings and proceed as follows:

♦ Go to **Settings > Network & Internet > Wi-Fi**

♦ Locate the active connection, long-tap it and select **Modify network**

♦ Expand the *Advanced options*, tap at **None** below *Proxy* and select **Manual**

♦ Enter the IP address from the previous step into the *Proxy hostname* field and the port into the *Proxy port* field

♦ Tap Save. <img width=40 src="https://user-images.githubusercontent.com/70295997/223303936-93820a76-13af-4d15-bd77-072e21d34273.png">

![2017 10 27 02 58 17-1_1](https://user-images.githubusercontent.com/70295997/223304321-36520bd1-e090-4cb3-b73c-3549e9996a3f.gif)

The settings on your device may look slightly different, but you should find the right area to modify the WiFi network. It will be located around the WiFi network, to which you are currently connected.

#### [Connect iOS Smartphone](https://youtu.be/vtSLoCC299U)

To connect an iOS device, follow these below captioned steps:

♦ Tap **Settings**

♦ Tap **WiFi**

♦ Tap **(i)** right to your selected WiFi network

♦ Scroll to the bottom to the **HTTP PROXY** section

♦ Tap **Manual**

♦ Enter the IP address from above in Server

♦ Enter the port from above in Port

## Capture and Decrypt SSL Traffic

As soon as customers require us to use Charles, they want to know what our mobile device is doing during its communication with their services. If this communication is encrypted, which is great for our day-to-day security, this traffic needs to be decrypted using a certificate. We're going to install this certificate to allow Charles to listen to that communication. Let's start with the desktops again.

### Install Desktop Certificate

Fortunately, Charles already includes this certificate and allows to install it using the menu easily. We have to circumvent a possible pitfall though. Just follow the below captioned process:

♦ Within Charles click **Help > SSL Proxying > Install Charles Root Certificate**

♦ In the new window click **Install certificate** and confirm the first screen unchanged

♦ Now select the second option **Place all certificates in the following store**

♦ Choose **Trusted Root Certification Authorities** as the store and finish the certificate installation wizard


![2017-10-26_22h09_25](https://user-images.githubusercontent.com/70295997/223305600-3a525c88-c267-4135-9437-4395c7669b0c.gif)
<img width="800" src="https://user-images.githubusercontent.com/70295997/223403200-2d226828-6555-4b59-9329-fb8c01908d2b.png">

### Install Certificate on Mobile Device

To install the certificate on a mobile device, just do the following:

♦ Be sure that the device is successfully connected to the Charles session:
  - Proxy is set to *Manual* and configured in the WiFi settings
  - Disconnect any active **VPNs** to avoid issues during the Charles session
  - Charles is running and the permission for the device has been granted
  - Browse on the phone and new logging entries appear within Charles

♦ Head to the address chls.pro/ssl (which leads to charlesproxy.com/getssl/) on the mobile device

♦ This downloads the certificate and should automatically open an installation prompt

♦ You may insert a name for the certificate like Charles Proxy, if needed, and confirm the installation

♦ Use Google and try searching for *iOS install certificate* for instance, if the installation process is unclear

####  iOS 10.3 or higher

If using iOS 10.3 or higher, additionally follow these steps to trust the certificate:

♦ Navigate to **Settings**

♦ Tap **About**

♦ Tap **Certificate Trust Settings** (bottom of the list)

♦ Trust the *Charles Root Certificate*

### Enable HTTPS Proxying

As our devices are set up for SSL logging now, we just have to enable SSL proxying within Charles as follows:

♦ Within Charles click **Proxy > SSL Proxying Settings...**

♦ In the *SSL Proxying* tab tick **Enable SSL Proxying** and click the **Add** button below

♦ Enter an asterisk <code>*</code> as Host and <code>443</code> as Port

♦ Now click **OK** and **OK** again

![2017-10-26_22h24_02](https://user-images.githubusercontent.com/70295997/223309814-862717f2-2e99-47f8-8566-6cc0fec1fc1a.gif)

  Restart Charles afterwards.

#### Tailor Coverage to Specific Needs

Above, we entered <code>*</code> as the *Host*. This *wildcard* character enables the SSL proxying for every possible web address or service we may visit. Though we might want to tailor the proxying, and therefore logging, to our needs via specifically including certain addresses or parts of addresses. Using wildcards provides a very versatile way of filtering specific URLs, which we want to cover.

This can become very handy, if we want to limit the coverage to an app or page under test. Let me provide some examples:

- <code>*google*</code> would cover every traffic from and to *google*, which includes *photos.google.com*, *google.com/mail* and so on
- <code>photos.google</code> would include everything from and to *photos.google.com*, but not *google.com/mail* for instance
- <code>google.com/mail</code> would cover the entire *mail* section, but no other section or *photos.google.com*. Though it would cover *photos.google.com/mail/...* if such websites existed.

So we take the relevant part of the address, which may include/exclude or be limited to sub-domains like *calendar* in <code>calendar.google.com</code> and replace the rest of the address with a <code>*</code> to allow every string or even no string (zero or more characters) in its place. You can also use the wildcard <code>?</code>, which replaces exactly one single character. So <code>go?gle</code> would match *google* or *goggle*, but not *gogle* or *googgle*.

## Capture SSL Logs

Now as Charles is running with the right settings, as the certificates have been installed, as our devices are configured to use Charles on our computer, and as SSL proxying is enabled, we're good to go!

Let's conclude the steps to collect logging information and to export them for to the benefit of a bug report:

♦ Clear the Charles log using the broom button

♦ Be sure that logging is active (red button in the toolbar)

♦ Perform actions or steps to reproduce an issue

♦ Stop the logging by clicking the red button

♦ Head to **File > Save Session as...**

♦ Choose a folder and pick a file name (don't use periods in the name)

♦ Upload the log ending with <code>.chls</code> to the bug report <img width=40 src="https://user-images.githubusercontent.com/70295997/223303936-93820a76-13af-4d15-bd77-072e21d34273.png">

### Tidy up

After you have finished your Charles session, make sure to close the software and to revert your WiFi settings on the mobile devices to their prior state. Hence we set the Proxy to **None** again, in the WiFi settings. We also remove the certificate from the devices if they are our privately used desktops, smartphones and tablets and not only meant for testing. 

If you ever want to start logging in the future, start Charles and add the IP address and port to your WiFi settings again. If the certificate was removed, remember to add it back too.

<img src="https://user-images.githubusercontent.com/70295997/223315240-010ee171-e169-4ed2-aaa6-ebf37540c714.png" width=40> Happy logging! 

