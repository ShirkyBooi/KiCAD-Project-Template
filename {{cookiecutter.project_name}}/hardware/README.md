# KiCad Guide for {{cookiecutter.project_name}}

KiCad is an open-source software suite for electronic design automation (EDA), facilitating the design of schematics for electronic circuits and their conversion into printed circuit board (PCB) layouts.

Upon creating your project using the cookiecutter template, several files and folders are generated, each with their specific use within the KiCad suite.

## Project Files and Folders

Your project will be named `{{cookiecutter.project_name}}.kicad_pro`. This is the main project file that manages all the individual files related to your project. Open this file with KiCad to start your project.

Here's a brief overview of the files and folders you'll encounter:

- `{{cookiecutter.project_name}}.kicad_pcb` - This file contains the PCB design. Do not open this file directly; instead, access it through the KiCad project interface.
- `{{cookiecutter.project_name}}.kicad_sch` - This file contains the schematic. Like the PCB design file, this should be accessed through the KiCad project interface and not opened directly.
- `{{cookiecutter.project_name}}.kicad_prl` - This file contains preset information about the PCB.
- `fp-lib-table` and `sym-lib-table` - These files map the project to the components library.
- `KiCAD Libraries/` - This folder contains a git submodule of our KiCad library. See the README inside the folder for more information.

## Getting Started

You will need KiCad version 7 installed on your system to open the project. If KiCad is installed, it should automatically associate the `.kicad_pro` file extension with itself.

To start working on your project, simply open `{{cookiecutter.project_name}}.kicad_pro`. This will open the project manager interface, from where you can access various tools such as the Schematic Editor, Symbol Editor, PCB Editor, Gerber Viewer, Image Converter, Calculator Tools, Drawing Sheet Editor, and the Plugin and Content Manager.

KiCad provides several other tools to help you in your design process:

- **Gerber Viewer:** This tool allows you to view your Gerber files from a similar perspective as the manufacturer.
- **Image Converter:** This tool can convert images to silkscreen for PCB. Supported file types include bmp, png, jpeg, tiff, and others.
- **Calculator Tools:** For advanced designs, these calculators can assist with calculating desired track widths, temperature ranges, radio frequency impedance control, etc.
- **Drawing Sheet Editor:** This tool allows you to edit the schematic and PCB drawing sheet templates. Please refrain from editing the templates unless necessary.
- **Plugin and Content Manager:** A one-stop shop for very useful plugins that can be installed and updated from within KiCad.


## Schematic Editor

The Schematic Editor is where you will design your circuit. It's equipped with many tools to help you draw, annotate, and validate your schematic. The fields on the bottom right are filled out by the template; avoid editing them unless absolutely necessary to maintain consistency.

Below is a description of the main tools you will be using:

- **Select Items**: Used to select components or wires for moving or editing.
- **Highlight Net**: Highlights a selected net in the schematic.
- **Add Symbol**: Used to place a symbol in your schematic.
- **Add Power Symbol**: Used to place a power symbol like VCC or GND.
- **Add Wire**: Draws a wire between components.
- **Add Bus**: Creates a bus for grouping multiple signals.
- **Add Wire Bus**: Allows you to connect multiple wires to a bus.
- **No Connect Flag**: Indicates a pin that is intentionally left unconnected.
- **Add Wire Joint**: Creates a junction for connecting wires.
- **Add Net Label**: Adds a label to a wire, which can be used to connect distant wires.
- **Add Hierarchical Sheet**: Creates a hierarchical sheet for modular schematic design.
- **Add Text**: Adds custom text annotations.
- **Add Image**: Inserts a custom image.
- **Delete Clicked Items**: Removes items clicked with this tool.
- **Edit Schematic Setup**: Opens the schematic setup options.
- **Rotate Component Counter-Clockwise**: Rotates selected components counter-clockwise.
- **Rotate Component Clockwise**: Rotates selected components clockwise.
- **Flip Component Top to Bottom**: Flips selected components top to bottom.
- **Flip Component Left to Right**: Flips selected components left to right.
- **Run ERC**: Performs Electrical Rule Check.
- **Run Footprint Association Tool**: Opens the CvPCB tool for associating footprints to schematic symbols.
- **Mass Edit Fields**: Allows you to edit fields of multiple components at once.

When starting a schematic, use the 'Add Symbol' button to place all your components. Connect everything with wires or netlabels. For complex designs, consider using hierarchical sheets to avoid clutter. You can save hierarchical sheets by name in the same directory. They will appear on the left on the schematic hierarchy, and you can use this tab to move between sheets.

Once done, use the 'Assign Footprints' button to ensure all components have the correct footprint, and the 'Mass Edit Fields' button to make sure all your component part numbers and minimum component fields are filled out.

## PCB Editor

Once you've designed your schematic, it's time to start on your PCB. Open your project's `.kicad_pcb` file, which should show a 50x50mm PCB template with your project name, logo, and magic number.

You can modify the size of your PCB to fit your requirements. The grid and placement origin are pre-set, so you can directly adjust the dimensions using the edge cuts border. Use the "Update PCB from Schematic" button (or F8) to import your components from the schematic. After confirming no errors, you can start placing your components and routing your design.

Here's a list of important tools:

- **Toggle Ratsnet**: Toggles the visibility of unconnected wires (the "rats nest").
- **Toggle Highlight Selected Layer**: Highlights the currently active layer.
- **Highlight Net**: Highlights the selected net on the PCB.
- **Show filled zones**: Toggles the display of filled zones.
- **Show only Zone outlines**: Toggles the display of zone outlines.
- **Show only pad outlines**: Toggles the display of pad outlines.
- **Show only via outlines**: Toggles the display of via outlines.
- **Show only track outlines**: Toggles the display of track outlines.
- **Toggle Appearance Manager**: Toggles the appearance manager, which controls layer visibility and colors.
- **Toggle Properties Manager**: Toggles the properties manager, which allows you to adjust the properties of individual components, tracks, and more.
- **Select Items**: Allows you to select components or traces for moving or editing.
- **Add Footprint**: Allows you to add a footprint to the PCB.
- **Route Trace**: Allows you to manually route a trace.
- **Route Differential Pair**: Allows you to route a differential pair.
- **Tune Track**: Adjusts the length of a track for timing purposes.
- **Tune Differential Pair**: Adjusts the length of a differential pair.
- **Add Filled Zone**: Creates a filled zone on the PCB.
- **Add Keepout Area**: Designates an area where components or tracks cannot be placed.
- **Draw Line**: Allows you to draw lines on the PCB.
- **Draw Arc**: Allows you to draw arcs.
- **Draw Rectangle**: Allows you to draw rectangles.
- **Draw Circle**: Allows you to draw circles.
- **Draw Polygon**: Allows you to draw polygons.
- **Add Text**: Adds custom text to the PCB.
- **Add TextBox**: Adds a textbox to the PCB.
- **Add Dimension**: Adds dimension markers to the PCB.
- **Delete Items**: Removes selected items from the PCB.
- **Place Position Grid Origin**: Sets the origin of the grid.
- **Measure**: Allows you to measure distances on the PCB.
- **DRC**: Performs Design Rule Check.
- **Add Teardrops**: Adds teardrops to vias and pad-to-track connections to prevent drill breakout.
- **Remove Teardrops**: Removes teardrops from the PCB.
- **Cleanup Tracks and Vias**: Cleans up redundant or unnecessary tracks and vias.
- **Manage Libraries**: Opens the footprint library manager.
- **3D Viewer**: Opens a 3D view of the PCB.

## Manufacturing File Generation

Generating manufacturing files is critical for transforming your design into a physical PCB. Depending on where you're getting the board manufactured, there are different ways to do this.

The most generic way is to navigate to the "Plot" button at the top left or "Fabrication Outputs" and click "Gerber". Set the output directory to the production folder under the Gerber folder. For a 4-layer board, include the following layers: F.Cu, In1.Cu, In2.Cu, B.Cu, F.Paste, B.Paste, F.Silkscreen, B.Silkscreen, F.Mask, B.Mask, Edge.Cuts. Always make sure DRC passes before proceeding. Click "Plot" and then "Generate Drill Files". This will create the Gerber files for manufacturing, allowing you to purchase the standalone PCB.

An alternative method, which is recommended for JLCPCB, is to use the Fabrication Toolkit Plugin, which you can install from the Plugin Manager. This plugin adds a button at the top right that generates all files for the Bill of Materials (BoM), Pick and Place (PnP), and Gerbers, all perfectly zipped and ready to go.

The Interactive HTML BoM plugin is also recommended. Use it to generate an interactive BoM by clicking one button, adjusting some parameters, and saving the iBoM in the BoM folder. This provides the manufacturer with a clear view for component placement.

Pick and Place files are necessary for the manufacturer to correctly place components on your board. These can be generated by the JLC Fab Kit, or manually by choosing "Component Placement" under Fabrication Outputs.

You can export the PCB 3D model via "Export VRML" or "Export STEP". Note that if you use a mix of WRL and STEP files for your models, your final model will be incomplete.

Lastly, you need to provide the manufacturer with additional information including PCB Qty, Assembled Qty, PCB Thickness, PCB Soldermask Colour, Surface Finish, Copper Weight, Via Tenting, Castellated Holes, Impedance Control, Stackup, and Via Precision.

## Plugins

KiCAD's functionality can be extended through the use of plugins. The following plugins are recommended and can be installed via the KiCAD Plugin Manager:

- **Interactive Html BoM (iBOM) Plugin**: Generates an interactive Bill of Materials (BoM) and provides component placement visualization.
- KiKit Plugin: Enables PCB panelization, optimizing the layout for production and maximizing PCB utilization.
- Archive 3D models Plugin: Consolidates and maps 3D models in one place for accurate component placement visualization.
- **JLC PCB Fabrication Toolkit Plugin**: One-click generation of Gerber files, BoM, and Pick and Place files, streamlining the transition from design to production.
- Freerouting Plugin: Optional autorouting tool for PCB layout, though manual routing is recommended for optimal control and signal integrity.
- JLC2KiCAD_lib by TousstNicolas: Script to convert components from EasyEDA, JLC, or LCSC formats to KiCAD format.

## General Tips

- You can use the `Insert` button on your keyboard to repeat the last placed or routed wire on the schematic spaced equally below it. It also increments the last digit of a netlabel, use it to quickly label GPIO0 to GPIO20 etc and wire underneath them.
- Visit the official KiCAD documentation [here](https://docs.kicad.org/) particularly I recommend reading the Getting Started Guide, Schematic Editor, and PCB Editor sections, especially if you are new to KiCAD.
- Udemy offers many excellent courses if you're new to PCB Design; they're definitely worth checking out during a sale.
