# Introduction

Hello and welcome to module 6 of the NetBox 'Zero-to-Hero' course. In [Module 5: Making the Connections](modules/5-making-the-connections/5-making-the-connections.md),  Eric added the cables and connections required to hook the devices in the new Brisbane branch office network together.  In this module, Susan will be adding the required Wireless LANs, and using some simple Python scripts to interact with the NetBox REST API.  

By the end of this module you will be able to:
- Describe how NetBox models Wireless LANs
- Use simple python scripts to read from and add data to the NetBox database via the REST API

## Why Use Python Scripts With NetBox? 
If you have been through the previous modules of this course you will know that it's easy to add data manually via the Web Interface, but when you are dealing with a lot of data that can quickly become tedious and is error prone. Using simple python scripts can both save you time and reduce errors. 

Getting started with Python is super easy and a lot of fun too! The [simple scripts](../../python_scripts/) included in the Git repository for this course will get you up and running quickly and within a few minutes you can be interacting with the NetBox database programmatically via the REST API.

Also, as any Network Engineer / IT Pro looking to expand their skill set knows, Automation is becoming critical for managing modern networks, so by adding some basic Python coding skills to your armory, you will set yourself up for long term success in your career.

## Get Hands On
If you'd like to follow along with the examples used in this course, it's super easy to do, and you have a few options: 
1.  Run NetBox as a container with [NetBox Docker](https://github.com/netbox-community/netbox-docker) - This is the quickest way to get your own dedicated NetBox instance going and it only takes a few minutes to spin up on your laptop!
2.  Follow the [official documentation](https://docs.netbox.dev/en/stable/installation/) and do a full installation all the NetBox components. These instructions have been tested on Ubuntu and CentOS Linux.
3.  Use the public [demo instance](https://demo.netbox.dev/) of NetBox   

The software versions used in the video for this module are: 
- `NetBox v3.3.2`
- `Python 3.8.9`
- `python-dotenv v0.21.0`

## Setting Up Your Python Environment
Follow these [simple steps](../../python_scripts/readme.md) to set up Python on your own system, so you can follow along running the python scripts.

## Modelling Wireless LANs in NetBox
You can model Wireless LANs (and Wireless point-to-point links) in NetBox just as you can model physical cabled networks. You can create self-nesting Wireless LAN Groups, and can also (optionally) bind Wireless LANs to particular VLANs. You can also (optionally) define the authentication parameters - Type, Cipher and PSK, for each SSID (Service Set Identifier).

## The Project - New Brisbane site Wireless LANs
Susan has planned the following Wireless LANs for the new Brisbane site, and this needs to be added to NetBox. 

| SSID | Description | WLAN Group | VLAN ID | Auth Type | Auth Cipher | Auth PSK |
| --- | --- | --- | :---: | --- | :---: | --- |
| B_WIFI | Branch Office Wifi | Asia_Pacific_WLANs | 30 | wpa-enterprise | aes | 5up3r5ecr3tK3y |
| G_WIFI | Guest Wifi | Asia_Pacific_WLANs | 40 | wpa-enterprise | aes | M3g45ecr3tK3y |

## Video - Adding Wireless LANs to NetBox
OK, so that's the planning and design work done - now onto the demo! This video will step you through how to populate NetBox with Wireless LAN data, and then to view that data in the Web Interface. As always the best way to understand the power of NetBox is to dive right in, so let's get started!

If you are following along you can find the [python scripts](../../python_scripts/) in course Git Repository.

<!-- link to video here -->

In this module you have learned how NetBox Models Wireless LANs, and how to add Wireless LAN data using simple Python scripts.

In the next module you will learn how to...

## Useful Links
- [Official NetBox Documentation](https://docs.netbox.dev/en/stable/)
- [NetBox Docker](https://github.com/netbox-community/netbox-docker)