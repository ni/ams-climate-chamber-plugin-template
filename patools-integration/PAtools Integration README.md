# PAtools Integration

[This](https://github.com/ni/bls-capabilities/blob/main/PAtools%20Integration%20README.md) document describes the process of integrating a new BLS plugin/Driver in PAtools using the Template_PowerSupply_BLS module. For a Cycler the steps are identical, instead of the Template_Power_Supply_BLS module the Template_ClimateChamber_BLS module is used. 

There is only one additional Initialization of Variables Group "Template_ClimateChamber_BLS_Stability" in the config folder. Here one can parameterize the variables for checking temperature and humidity stability.
