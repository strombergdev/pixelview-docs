---
layout: default
title: Stream with OBS
nav_order: 1
---

# Setup OBS

## Table of Contents
+ [Getting started](#getting_started)
+ [View stream](#viewstream)
+ [Change bitrate](#changebitrate)
+ [Troubleshooting](#troubleshooting)


## Getting Started <a name = "getting_started"></a>

1. [Download](https://obsproject.com/) the latest version of OBS.

2. Open settings.

![](https://pixelview.io/wp-content/uploads/2021/09/OBS_Instructions_1.png)

3. Choose Custom and paste the Server address you’ve received from us. Leave Stream Key blank.

![](https://pixelview.io/wp-content/uploads/2021/09/OBS_Instructions_2.png)

4. Go to output and set bitrate. We recommend around 6 Mbit/s (6000 Kbps). Please don’t stream at higher bitrate than 12 Mbit/s.

Set CPU preset and Tune to “ultrafast” and “zerolatency” for lowest latency. 

![](https://pixelview.io/wp-content/uploads/2021/09/Screenshot-2021-09-22-at-18.33.34.png)

5. Click Start Streaming.

![](https://pixelview.io/wp-content/uploads/2021/09/OBS_Instructions_4.png)

### Potential error
If you get an error message in OBS that it can’t connect to the server. First go to the login.pixelview.io/123456 page and click the link to watch the stream and enter your name. Then try to start the stream again in OBS. You might need to refresh the viewer as well after a while. The reason for this error is that the port on the server is not opened until someone is watching the stream. 

![](https://pixelview.io/wp-content/uploads/2021/12/Error_Messsage_OBS.png)

## View the Stream <a name = "viewstream"></a>
Login to the admin page using your unique link and password. 
```
login.pixelview.io/xxxxxx
```
The simplest way to view the stream is using the "Web link with embedded password”. This link has everything embedded so just send it to your clients and they will see the stream immediately. 

You can also choose to send the link with a manual password.

Use Safari for best quality and latency.

Best color accuracy and quality is in the iPhone, iPad or Apple TV apps. Download [Pixelview Player](https://apps.apple.com/se/app/pixelview-player/id1570446440) from the app store and enter the Stream ID and Password.

## Change bitrate <a name = "changebitrate"></a>
- Adjust the bitrate in OBS by going to Settings, Output and setting it to a value between 1000-12000 Kbps. 

- Then go to the login.pixelview page and change Chrome/Firefox h264 bitrate as well to match.

## Troubleshooting <a name = "troubleshooting"></a>
If you are seeing artefacts or other glitches in the stream there are a couple of settings to change. 

### Latency
In the SRT protocol, this parameter is used to mitigate bad network between you and the server. It should be no less than twice the round-trip between encoder and ingest server. Increasing it will lead to slighly longer latency but a more stable stream.

- Add the following to the end of your server URL. 
```
&latency=200000
i.e srt://us-1.pixelview.io:1234?passphrase=xxxxxx&latency=200000
```
This will increase the latency from the default 120 ms to 200 ms. You can try with different numbers until you get a stable stream. 

### Buffer
The buffer is used to help a poor connection between the stream server and your viewers. 
- Open the admin page at login.pixelview and increase the buffer.  