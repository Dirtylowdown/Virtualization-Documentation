---
title: Integration components available for virtual machines not connected to Windows Update
description: Learn about the available integration components for virtual machines not connected to a Windows update using Hyper-V.
author: sethmanheim
ms.author: mabrigg
date:       2015-07-24 10:42:00
ms.date: 07/24/2015
categories: hyper-v
---
# Integration components available for virtual machines not connected to Windows Update

In Technical Preview, Hyper-V began delivering integration components through Windows Update ([see blog for more information](https://techcommunity.microsoft.com/t5/virtualization/hyper-v-integration-components-are-available-through-windows/ba-p/382235 "see blog for more information")). Pushing updates through Windows Update was a good first step -- it is the easiest way to keep integration components up to date. There are situations, however, where the virtual machine isn't connected to Windows Update and sometimes it is more convenient to patch an offline (turned off) virtual machine. Now, in addition to receiving integration component updates automatically through Windows Update, you can also update integration components on virtual machines that aren't running or aren't connected to Windows Update using the cab files available in [KB3071740](https://support.microsoft.com/kb/3071740). (Last time I looked, the download links weren't working. ****** **Note:** Everything in this blog post applies to Server 2016 Technical Preview or Windows 10 and associated preview builds or later. The instructions here should work for virtual machines on Server 2012R2/Windows 8.1 but that is not tested or supported! ** 

## Updating integration components on an virtual machine that is not turned on

Here's a script that updates integration components. It assumes you are updating a virtual machine from the Hyper-V host. If the virtual machine is running, it will need to be stopped (the script below does this for you) and you'll need to locate its VHD (virtual hard drive). ** For step by step instructions with explanations read [this post](https://techcommunity.microsoft.com/t5/virtualization/how-to-install-integration-services-when-the-virtual-machine-is/ba-p/382044) but use the cabs from the KB article. Run the following in PowerShell as administrator. You will need the path to the cab file that matches the operating system running in your virtual machine and the path to your VHD. 

## Update integration components inside the virtual machine without using Windows Update

These instructions assume you are running on the virtual machine you want to update. First, find the cab file that matches the operating system running in your virtual machine and download it. Run the following in PowerShell as administrator. Remember to set the right path to the downloaded cab file.  $integrationServicesCabPath="C:\Users\sarah\Downloads\windows6.2-hypervintegrationservices-x86.cab"  #Install the patch Add-WindowsPackage -Online -PackagePath $integrationServicesCabPath Now your virtual machines can all have the latest integration components! Cheers, Sarah
