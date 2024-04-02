---
title: DPM for data backup/recovery of virtualized apps and environments
keywords: virtualization, virtual server, virtual pc, blog
description: Congratulations to the Microsoft Storage Solutions team for releasing Service Pack 1 for System Center Data Protection Manager 2007.
author: scooley
ms.author: scooley
ms.date: 1/13/2009
ms.topic: article
ms.assetid: 
---

# DPM for data backup/recovery of virtualized apps and environments

We want to congratulate the Microsoft Storage Solutions team for releasing Service Pack 1 for System Center Data Protection Manager 2007.

SP1 for DPM 2007 brings some great new capabilities for protecting Hyper-V environments.  Most notably, of course, is the ability to protect guests within Hyper-V environments, often without downtime (for those guests running a Windows operating system that supports VSS).  Also new for DPM with SP1 is the ability to run the DPM server on the Hyper-V host itself, so that the DPM server can protect the guests from the host viewpoint, within the same physical server - to disk, to tape and even to the cloud. 

And unlike other (shall-not-be-named) virtualization platforms’ backup mechanisms, DPM does _not_ require a SAN and does _not_ require 3rd party backup software or add-ons.   It’s an all Microsoft backup and recovery solution for Microsoft’s virtualization platform.

For more details on the SP1 release for DPM 2007, check out:

·         Bala’s executive [viewpoint on DPM 2007 sp1](https://techcommunity.microsoft.com/t5/system-center-blog/bg-p/SystemCenterBlog)

·         Some early SP1 customers are also blogging about their experiences and you can see at these links – [ICON](https://techcommunity.microsoft.com/t5/system-center-blog/bg-p/SystemCenterBlog) & [Convergent Computing]https://techcommunity.microsoft.com/t5/system-center-blog/bg-p/SystemCenterBlog)

·         A feature overview of DPM SP1 

The DPM folks have dedicated resources on “ ** _How to protect virtualized environments with DPM 2007_** ” – [here](https://www.microsoft.com/DPM/virtualization). And a very cool podcast showing how to protect Hyper-V with DPM 2007 SP1 

Congrats to the DPM crew – and nice job on backing up Hyper-V !!!

Patrick
