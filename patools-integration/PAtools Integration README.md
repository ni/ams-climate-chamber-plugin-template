# PAtools Integration

[This](https://github.com/ni/ams-capabilities/blob/main/PAtools%20Integration%20README.md) document describes the process of integrating a new AMS plugin/Driver in PAtools using the Template_AMS_PowerSupply module. For a Climate Chamber the steps are identical, instead of the Template_AMS_PowerSupply module the Template_AMS_ClimateChamber module is used.

There is only one additional Initialization of Variables Group "Template_AMS_ClimateChamber_Stability" in the config folder. Here one can parameterize the variables for checking temperature and humidity stability.