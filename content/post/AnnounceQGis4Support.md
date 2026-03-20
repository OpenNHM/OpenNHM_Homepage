---
title: "AvaFrame and OpenNHM QGIS Connector now available for QGIS 4.0"
date: 2026-03-20T00:00:00+01:00
author: "Felix"
draft: false
tags:
  - avaframe
  - openNHM
  - announcement
  - qgis
description: "Early adopter instructions for running AvaFrame with QGIS 4.0 using the new
OpenNHM QGIS Connector."
---

QGIS 4.0 is here, and so is our support for it. We have a pre-release of AvaFrame and a new
QGIS connector ready for early adopters to try out.

The **OpenNHMQGisConnector** replaces the previous AvaFrameQGisConnector. The new connector
is the home for all OpenNHM tools going forward, including upcoming additions for debris flow
modeling.

## How to get started

### 1. Install the AvaFrame pre-release

Open the **OSGeo4W Shell** that matches your QGIS version (important if you have multiple
versions installed) and run:

    pip install avaframe==2.0rc3

### 2. Download the connector

Get the OpenNHMQGisConnector zip from the release page:

https://github.com/OpenNHM/AvaFrame/releases/download/2.0rc3/OpenNHMQGisConnector.zip

### 3. Install the connector in QGIS

Open QGIS, go to **Plugins > Manage and Install Plugins**, choose **Install from ZIP** and
select the downloaded file. After installation, you should find the OpenNHM tools in your
**Processing Toolbox**.

**Note:** The versions mentioned above may not be the latest. Check
[GitHub Releases](https://github.com/OpenNHM/AvaFrame/releases) for the newest connector zip
and [PyPI](https://pypi.org/project/avaframe/#history) for the latest AvaFrame package version.

## Feedback

This is a pre-release -- if you run into issues, please let us know through our usual
channels or open an issue on
[GitHub](https://github.com/OpenNHM/AvaFrame/issues).
