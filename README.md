# Intro to Charles Web Proxy for Desktops and Smartphones

Some test cycles require extended logging of the internet traffic from/to your device or a connection routed through a proxy server. For that purpose, you'll have to deal with the proxy server software, such as Charles Web Proxy.

Let's go throgh the installatio and configuration steps:

✰ Download and install Charles

✰ Connect a Smartphone or Tablet to Charles

✰ Capture SSL traffic using Charles

✰ Export device logs for attaching them to bug reports

## Download and Install

Although Charles is not an open source software or a free tool, a demo version is available. It can be downloaded and used for free, but limits each session to 30 minutes. Consequently, you have to restart the software now and then, if you want to use it for a more extended period. 

Download the appropriate version of [Charles Proxy](https://www.charlesproxy.com/download/) for your OS.

<img width="800" src="https://user-images.githubusercontent.com/70295997/223290039-0a68dbd5-123e-4614-a880-776524a9cd54.png">

Once you have finished the installation, start the software. You will have to wait 10 seconds at every start.

## Connect Devices

As Charles is running now, we want to route all the network traffic from and to our devices through it. Depending on the device you plan to use, please perform the following steps matching your device(s).

### Desktops

You are already done! As soon as Charles is running, it will automatically capture and record all browser traffic. This procedure typically covers the most common browsers like Chrome, Firefox, Safari, and Edge. You can quickly check the proxy connection by following these steps:

♦ Ensure that Windows Proxy is enabled in the Proxy menu.
  
  <img width="800" src="https://user-images.githubusercontent.com/70295997/223293316-92174d0f-3b47-452c-9b5e-34424a08fb9c.png">

♦ Click the 🧹 broom button (leftmost) in the Charles toolbar to clean the logs.

<img width="800" src="https://user-images.githubusercontent.com/70295997/223294009-82ac2a9a-1844-492f-9e5f-ff06417cd2f8.png">

♦ Open your browser and navigate to a random site.

♦ You'll see new log entries popping up in the Charles log.


♦ You can also pause and resume the logging at any time using the second red/grey button in the toolbar.

<img width="600" src="https://user-images.githubusercontent.com/70295997/223294999-aef56c65-9f69-4a50-8a04-6848c91a092f.png">

