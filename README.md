# Intro to Charles Web Proxy for Desktops and Smartphones

Some test cycles require extended logging of the internet traffic from/to your device or a connection routed through a proxy server. For that purpose, I have to deal with some proxy server software, such as Charles Web Proxy.

Let's go throgh the installatio and configuration steps:

✰ [Download and install Charles](https://github.com/lana-20/charles-setup/blob/main/README.md#download-and-install)

✰ [Connect a Smartphone or Tablet to Charles](https://github.com/lana-20/charles-setup/blob/main/README.md#connect-devices)

✰ [Capture SSL traffic using Charles]()

✰ [Export device logs for attaching them to bug reports]()

## Download and Install

Although Charles is not an open source software or a free tool, a demo version is available. It can be downloaded and used for free, but limits each session to 30 minutes. Consequently, I have to restart the software now and then, if I want to use it for a more extended period.

<img width="600" src="https://user-images.githubusercontent.com/70295997/223296577-314ac68f-8ac3-4f2f-8ec0-aa908d9935ca.png">

Download the OS-appropriate version of [Charles Proxy](https://www.charlesproxy.com/download/).

<img width="800" src="https://user-images.githubusercontent.com/70295997/223290039-0a68dbd5-123e-4614-a880-776524a9cd54.png">

Once the installation is finished, start the software. I have to wait 10 seconds at every start.

## Connect Devices

As Charles is running now, I want to route all the network traffic from and to my devices through it. Depending on the device I plan to use, perform the following steps matching the device(s).

### Desktops

I am already done! As soon as Charles is running, it automatically captures and records all browser traffic. This procedure typically covers the most common browsers like Chrome, Firefox, Safari, and Edge. I can quickly check the proxy connection by following these steps:

♦ Ensure that **Windows** or **macOS** Proxy is enabled in the Proxy menu.
  
  ![2017-10-26_20h21_22_3](https://user-images.githubusercontent.com/70295997/223298601-12088334-9461-430a-9f3c-f3a457858bf1.gif)
  <img width="800" src="https://user-images.githubusercontent.com/70295997/223293316-92174d0f-3b47-452c-9b5e-34424a08fb9c.png">

♦ Click the 🧹 broom button (leftmost) in the Charles toolbar to clean the logs.

<img width="800" src="https://user-images.githubusercontent.com/70295997/223294009-82ac2a9a-1844-492f-9e5f-ff06417cd2f8.png">

♦ Open the browser and navigate to a random site.

♦ Observe new log entries popping up in the Charles log.

<img width="800" src="https://user-images.githubusercontent.com/70295997/223295849-98a59ccb-fec6-467a-89dd-07c9f299b1ec.png">

♦ I can also pause and resume the logging at any time using the second red/grey button in the toolbar.

<img width="600" src="https://user-images.githubusercontent.com/70295997/223294999-aef56c65-9f69-4a50-8a04-6848c91a092f.png">

If I can see my log filling up, I'm good to go.

### Mobile Devices

Gather ② crucial pieces of information first.

Before I can configure my mobile device to use Charles, I need to know the IP address of my computer (running Charles) and the port. This can quickly be done as follows:

♦ Click **Help > Local IP Address** to locate the IP. The address consists of four blocks of one to three digits each. It most certainly starts with <code>192</code> and must not end with <code>1</code>. In my case it's <code>192.168.178.100</code>.

   ![2017-10-26_20h39_33](https://user-images.githubusercontent.com/70295997/223300255-ae04ed1b-f4ae-4abf-b7de-3624fd9b9edb.gif)

♦ 

♦ 

♦ 

♦ 








