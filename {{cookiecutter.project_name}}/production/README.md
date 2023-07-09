# Production for {{cookiecutter.project_name}}

Welcome to the Production section for the {{cookiecutter.project_name}} project. This section encompasses all the resources and files necessary for the manufacturing and assembly of the hardware design. This includes the Bill of Materials (BoM), Computer-Aided Design (CAD) models, Gerber files, and Pick and Place files.

## Bill of Materials (BoM)

The [Bill of Materials (BoM)](./bom/README.md) for {{cookiecutter.project_name}} can be found in this directory. The BoM is provided in both a CSV format and the interactive BoM (iBoM) format for easy reference and use.

## CAD

This directory hosts the [CAD models](./cad/README.md) of {{cookiecutter.project_name}}. These 3D models are provided in various file formats such as STEP, VRML, STL, and Fusion 360 for compatibility across various CAD software.

## Gerber

The [Gerber files](./gerber/README.md) for {{cookiecutter.project_name}} are stored in this directory. These files are essential for PCB fabrication and include specifications for copper layers, silk layers, solder paste layers, mask layers, drill files, and the board outline.

## Pick and Place

The [Pick and Place files](./pnp/README.md) for {{cookiecutter.project_name}} can be found in this directory. These files provide necessary component placement information for PCB assembly, including Gerber files with accurate component outlines and reference designators, and a CSV file detailing the positions and rotations of the components on the PCB.
