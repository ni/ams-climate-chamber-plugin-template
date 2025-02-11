# ams-climate-chamber-plugin-template

This repository contains a template for building a AMS Plugin for a Power Supply to use with PAtools.
It requires the [AMS Capabilities](https://github.com/ni/ams-capabilities).

## Supported Versions

- PAtools 8.4+
- LinuxRT 24Q2+
- LabVIEW 2023Q3+
- AMS Capabilities API 1.0+
- ADAS Replay HIL Development Suite 24Q1+

# Create your own plugin
Make sure you read the [AMS Capabilities README](https://github.com/ni/ams-capabilities). [Here](https://github.com/ni/ams-capabilities/blob/main/AMSTEMPLATES.md) it is described how to create your own plugin and how to test it.

# PAtools Integration
see [PAtools Integration Readme](/patools-integration/PAtools%20Integration%20README.md)


# Climate Chamber Plugin Description

* The climate chamber plugin takes in user inputs to control the system and values and then output the set values for items such as the temperature and humidity to test the DUT in extreme conditions.
* To initialize and close channels used in the climate chamber plugin, create channels.vi and destroy channels.vi use the close and initialize from the AMS capabilities Climate Chamber high level capability which initialize and close all of the VI and classes that are implemented.
* As a part of the simulation, some of the tasks that are done by the Process Data.vi include checking the range of current, voltage, and power, applying the gradient to control the rate at which the values change, simulating noise through the addition of random numbers, setting/resetting the error status and conditions if errors are present.

# Helper VIs
* Apply Gradient: Controls how the value of each element is changing over time
