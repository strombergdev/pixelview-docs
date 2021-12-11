---
layout: default
title: Setup Magewell encoder
nav_order: 2
---

# Setup Magewell Encoder

## Table of Contents
+ [Getting started](#getting_started)
+ [View stream](#viewstream)
+ [Change bitrate](#changebitrate)
+ [Connect to Wifi](#connecttowifi)
+ [Adjust color settings](#adjustcolorsettings)
+ [Troubleshooting](#troubleshooting)


## Getting Started <a name = "getting_started"></a>
- Connect SDI, ethernet and power.
- Login using the link written on the backside of the box. 

## View the Stream <a name = "viewstream"></a>
The simplest way to view the stream is using the "Web link with embedded password”. This link has everything embedded so just send it to your clients and they will see the stream immediately. 

You can also choose to send the link with a manual password.

On computers, use Safari for best quality as it supports the higher quality H265/HEVC compression sent from the box. Firefox and Chrome does not support h265, so they get a h264 that is transcoded on our servers.

Best color accuracy and quality is in the iPhone, iPad or Apple TV apps. Download [Pixelview Player](https://apps.apple.com/se/app/pixelview-player/id1570446440) from the app store and enter the Stream ID and Password.

## Change bitrate <a name = "changebitrate"></a>
The box is set to 6 Mbit when you get it which is a good mix between quality and bandwidth. If you want better quality, and your clients can support it, you can increase it up to 12 Mbit.

- Locate the encoders IP address on your network by checking your routers DHCP list. Then open it in your web browser. 192.168.1.207 for example.

- Login with the username Admin and the same password written on the backside of the box.

- Click “Encoding Parameters” and then Advanced settings. Change bitrate and save.

- Then go to the login.pixelview page and change h264 bitrate as well. This is the setting we use to generate the h264 for Chrome/Firefox on our server.

## Connect to Wifi <a name = "connecttowifi"></a>
- Locate the encoders IP address on your network by checking your routers DHCP list. Then open it in your web browser. 192.168.1.207 for example.

- Login with the username Admin and the same password written on the backside of the box.

- Click "Network" and find the Wifi settings, select "Change".

## Adjust color settings <a name = "adjustcolorsettings"></a>
- Locate the encoders IP address on your network by checking your routers DHCP list. Then open it in your web browser. 192.168.1.207 for example.

- Login with the username Admin and the same password written on the backside of the box.

- On the frontpage there is a button named "Color". Here you can adjust Brightness, Contrast, Hue and Saturation. 

- Click General on the left menu to access settings for Color Format and Quantization. 

## Troubleshooting <a name = "troubleshooting"></a>
If you are seeing artefacts or other glitches in the stream there are a couple of settings to change. 

### Latency
In the SRT protocol, this parameter is used to mitigate bad network between you and the server. It should be no less than twice the round-trip between encoder and ingest server. Increasing it will lead to slighly longer latency but a more stable stream.

- Locate the encoders IP address on your network by checking your routers DHCP list. Then open it in your web browser. 192.168.1.207 for example.

- Login with the username Admin and the same password written on the backside of the box.

- Click "Streaming Server" and "Edit". Increasing the latency value until you get a stable image. 

### Buffer
The buffer is used to help a poor connection between the stream server and your viewers. 
- Open the admin page at login.pixelview and increase the buffer.  