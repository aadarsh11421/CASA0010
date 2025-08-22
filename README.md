# Driving vs Behaviour Interactions in Delhi's Bus Rapid Transit Systems (BRTS)
This study investigates the Delhi Bus Rapid Transit (BRT) system using Agent-Based Modelling (ABM) to analyse the conflict between its rigid infrastructure and the region's fluid, non-lane-based driving culture. The research demonstrates that while the BRT improves bus performance, it does so at a significant cost to other motorized vehicles.

A microscopic traffic simulation of the Siri Fort intersection was developed in SUMO, calibrated with empirical data on traffic volume, signal timings, and vehicle parameters. The model employs the Intelligent Driver Model (IDM) and SL2015 lane-changing model to simulate agent behaviours, including 'normal' and 'aggressive' driver profiles, across low, medium, and high traffic flow scenarios.

Results reveal that the BRT system structurally disadvantages general motorized vehicle (MV) traffic, causing performance degradation even at low flows. Critically, at medium traffic volumes, the system reaches a tipping point, leading to a catastrophic, system-wide failure for MV traffic, while a non-BRT configuration remains congested but functional. The study also finds that aggressive driving offers only marginal benefits at near-capacity conditions and is futile in gridlock, demonstrating that infrastructure design and traffic volume are the dominant factors determining system stability.

The failure of the Delhi BRT was not an indictment of bus priority itself, but an outcome of a design incompatible with existing traffic demand. These findings underscore that for BRT systems to succeed in contexts with high-volume, heterogeneous traffic, they must be implemented with complementary measures to manage mixed-traffic flow and prevent systemic collapse.

# About the Repository
This project is organized into three main folders. The SUMO folder contains the BRT network system configuration with the standard vehicle demand and the BRT-specific Traffic Light System (TLS). The SUMO - No BRT folder includes the modified non-BRT network system configuration with its adjusted TLS. The BRT Aggressive folder contains the BRT network configuration with aggressive vehicle demand, where 10% of vehicles are assigned aggressive driving behavior. Additionally, the Output folder includes two Jupyter Notebook files: one converts SUMO’s XML outputs into CSV format, and the other uses these CSV files to generate network indicators.

# How to Run
The simulation can be executed using the provided SUMO configuration and network files. Below is a description of the key files:
  1. .net file – Defines the road network used for the simulation.
  2. .rou file – Specifies the vehicle demand, routes, and vehicle types.
  3. .netcfg file – A NetEdit configuration file used for editing and managing the network.
  4. _SumoSettings file – Stores the simulation settings used in SUMO (e.g., simulation parameters, processing).

## Steps to run the simulation:
  1. Open SUMO GUI (sumo-gui) or run it via the command line.
  2. Load the .sumocfg file (e.g., siriFort.sumocfg), which references the network, routes, and TLS configurations.
  3. Run the simulation. The defined demand and traffic light settings will be applied automatically.
  4. Outputs will be saved in the output folder if configured in the settings.
