# UNDER CONSTRUCTION
# GitHub Repo Template

GitHub Repo Template is a template for creation of open source projects made
available on GitHub. It includes a permissive open source license, a developer
certificate of origin, and a pull request template. This provides everything
necessary to have a properly licensed open source project.

## Using GitHub Repo Template

1. Clone or download this repository.
2. Copy its contents into your project (including the hidden .github directory). 
3. Customize each file to suit your project's needs (including the README). Look through the files for "TODO" and \<reponame\>, and replace with content appropriate to your project.
4. (Optional) Check out [GitHub Template Guidelines](https://github.com/cezaraugusto/github-template-guidelines) for ideas about how to customize your project.

TODO: describe a project in detail, what it does, how to use it, etc.

# Power Supply Plugin Description

* The power supply plugin takes in user inputs to control the system and values and then output the set values for items such as the voltage, power, and current of the device. The power supply is static and doesn't have a high current.
* To intialize and close channels used in the power supply plugin, create channels.vi and destroy channels.vi use the close and initialize from the BLS capabilities Power Supply high level capability which initialize and close all of the VI and classes that are implemented.
* As a part of the simulation, some of the tasks that are done by the process data.vi include checking the conditions that on off and output enable are set to true before setting values, checking the range of current, voltage, and power, applying the gradient to control the rate at which the values change, simulating noise through the addition of random numbers, setting/resetting the error status and conditions if errors are present, counting and resetting the watchdog, and selecting an output mode which uses arithmetic to output power and current.

# Helper VIs
* Control Mode Select: Reads the control mode (0, 1, 2) and outputs the current, power, and voltage accordingly. 0 is the default where all inputs are wired to their respective outputs. 1 multiplies current and voltage to output power. 2 outputs current by dividing power by voltage.
* Apply Gradient: Controls how the value of each element is changing over time
* Create element output: Takes each of the current, voltage, and power element inputs after they are passed through the Apply Gradient VI, and checks they are within the set max and min range and fixes them to be within range. If they aren't in range, an error is written to error channels. If output is enabled and it OnOff is true, there will be simulated noise added to each of the now in range elements, and the values will be passed to the outputs.
