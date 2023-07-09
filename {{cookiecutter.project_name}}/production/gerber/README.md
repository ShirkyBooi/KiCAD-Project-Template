# Gerbers

Include the Gerber files for {{cookiecutter.project_name}} in this section. These files are used for PCB fabrication.

## Required Gerber Files

Ensure that the following Gerber files are included for manufacturing {{cookiecutter.project_name}}:

- Copper Layers: `{{cookiecutter.project_name}}-F_Cu`, `{{cookiecutter.project_name}}-B_Cu` (top and bottom copper layers)
- Silk Layers: `{{cookiecutter.project_name}}-F_SilkS`, `{{cookiecutter.project_name}}-B_SilkS` (top and bottom silkscreen layers)
- Solder Paste Layers: `{{cookiecutter.project_name}}-F_Paste`, `{{cookiecutter.project_name}}-B_Paste` (top and bottom solder paste layers)
- Mask Layers: `{{cookiecutter.project_name}}-F_Mask`, `{{cookiecutter.project_name}}-B_Mask` (top and bottom solder mask layers)
- Drill Files: `{{cookiecutter.project_name}}-PTH` or `{{cookiecutter.project_name}}-NPTH` (NC drill file)
- Board Outline: `{{cookiecutter.project_name}}-Edge_Cuts`(board outline or edge cuts)

Please ensure that you generate or provide the appropriate Gerber files with the correct extensions for your PCB fabrication. These files are necessary for accurate manufacturing of the PCB.
