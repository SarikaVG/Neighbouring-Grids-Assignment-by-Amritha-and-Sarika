# Neighbouring-Grids-Assignment-by-Amritha-and-Sarika
EH2745: Computer Applications in Power Systems- Assignment 1. By Amritha Jayan and Sarika Vaiyapuri Gunassekaran

Objective: The objective of this code is to combine Python programming, CIM-XML modeling, and parsing techniques to build a power grid model using the Pandapower library. Specifically, the code merges Belgium (BE) and Netherlands (NL) MicroGrid configurations, walks through CIM-XML trees, identifies missing resource IDs, and plots the resulting merged grid.

Overview: 
The code achieves its objective by performing the following key steps:

1. XML Parsing: The code parses XML files (MicroGridTestConfiguration_T4_BE_EQ_V2.xml, MicroGridTestConfiguration_T4_BE_SSH_V2.xml, MicroGridTestConfiguration_T4_NL_EQ_V2.xml, and MicroGridTestConfiguration_T4_NL_SSH_V2.xml) using the xml.etree.ElementTree library.

2. Data Extraction: It extracts grid topology information such as AC Line Segments, Breakers, Busbar Sections, Connectivity Nodes, Energy Consumers, Generating Units, Power Transformers, Power Transformer Ends, Synchronous Machines, Terminals, and Voltage Levels.

3.Network Traversal: The code traverses the network to find missing resource IDs, focusing on connectivity nodes.

4.Pandapower Model Creation: It utilizes the Pandapower library to create a power grid model. The model includes buses, transformers, switches, loads, generators, and lines.

5.Plotting: The resulting merged grid is plotted using Pandapower's plotting functions.

Prerequisites: 
The code requires the following dependencies:
Python 3. x (Spyder Version 5)
Pandapower
Python environment with required libraries: xml.etree.ElementTree, pandapower, and pandapower.plotting.
CIM-XML files: MicroGridTestConfiguration_T4_BE_EQ_V2.xml, MicroGridTestConfiguration_T4_BE_SSH_V2.xml, MicroGridTestConfiguration_T4_NL_EQ_V2.xml, and MicroGridTestConfiguration_T4_NL_SSH_V2.xml.

Usage:
Ensure Python and required libraries are installed.
Place the CIM-XML files in the same directory as the script.
Run the script to generate the Pandapower model and plot the merged grid.

Functionality:
1.XML Parsing: The script reads and parses CIM-XML files for different equipment configurations in Belgium and Netherlands MicroGrids.
2.Data Extraction: The extract_grid_topology function extracts information about AC Line Segments, Breakers, Busbar Sections, Connectivity Nodes, Energy Consumers, Generating Units, Power Transformers, Power Transformer Ends, Synchronous Machines, Terminals, and Voltage Levels.
3.Network Traversal: The code identifies missing resource IDs in Connectivity Nodes between Belgium and Netherlands configurations.
4.Pandapower Model Creation: It creates a Pandapower model based on the extracted grid topology, including buses, transformers, switches, loads, generators, and lines.
5.Plotting: The Pandapower model is plotted using the pandapower.plotting.simple_plot function, providing a visual representation of the merged grid. In the plot left side is NL and right side is BE, between them there are 5 connection nodes found and merged together.

Plot:
![image](https://github.com/SarikaVG/Neighbouring-Grids-Assignment-by-Amritha-and-Sarika/assets/129281256/4bbedbd7-e8ca-42c6-8708-93722f87355f)
