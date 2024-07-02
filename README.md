# bls-climate-chamber-plugin-template

This repository contains a template for building a Battery Lab Software Plugin for a Climate Chamber.

# How to Use Template

1. Clone or download this repository.
2. Copy its contents into your project (including the hidden .github directory). 
3. Customize each file to suit your project's needs (including the README). Look through the files for "TODO" and \<reponame\>, and replace with content appropriate to your project.

# Creating the LabVIEW Plugin

## Supported Versions

- PAtools 8.4+
- LinuxRT 24Q2+
- LabVIEW 2023Q3+
- BLS Capabilities API 0.5+
- ADAS Replay HIL Development Suite 24Q1

1. Install the ADAS Replay and HIL AD Development Suite for LabVIEW.
1. Install the [BLS Capabilities API](https://github.com/ni/bls-capabilities).
1. Refer to the [ADAS Plugin Development](https://github.com/ni/adas-replay-hil-internal/wiki/Node-Development) to create your basic plugin.
1. Refer to the BLS Capabilities API Readme for more information.

## Package Deployer for BLS Plugins

The test/ plugin contains an example for a package which will install the lvlibp to the RT target. Follow these simple steps to update your Plugin.

1. Open your Plugin LabVIEW Project.
1. Right-click Build Specifications.
1. Select Package.
1. Under Source Files, select the lvlibp.
1. Select the blue arrow to add the lvlibp to the destination.
  - :cactus: LabVIEW will compile the lvlibp and automatically configure the directory.
1. Select Package and configure all the fields for your device.
1. Select OK.


# Climate Chamber Plugin Description

* The climate chamber plugin takes in user inputs to control the system and values and then output the set values for items such as the temperature and humidity to test the DUT in extreme conditions.
* To intialize and close channels used in the climate chamber plugin, create channels.vi and destroy channels.vi use the close and initialize from the BLS capabilities Climate Chamber high level capability which initialize and close all of the VI and classes that are implemented.
* As a part of the simulation, some of the tasks that are done by the Process Data.vi include checking the range of current, voltage, and power, applying the gradient to control the rate at which the values change, simulating noise through the addition of random numbers, setting/resetting the error status and conditions if errors are present.

# Helper VIs
* Apply Gradient: Controls how the value of each element is changing over time
