Readme.txt

📐 AutoLISP Routine – Total Length Calculator

This AutoLISP script calculates the total length of selected objects (lines, arcs, polylines, splines, etc.) in an AutoCAD drawing.
It then displays the result in the command line and inserts an MTEXT label into the drawing with the total length and units.

🚀 Features

Supports LINE, ARC, LWPOLYLINE, POLYLINE, SPLINE entities.

Reads drawing insertion units (INSUNITS) and appends the correct unit name (Millimeters, Meters, Feet, Inches, etc.).

Automatically scales values if drawing is set to mm but actual geometry is in meters.

Inserts result as MTEXT with height matching the drawing’s TEXTSIZE variable.

Simple command: TOTLEN.

📂 Installation

Save the script as TotLen.lsp.

In AutoCAD, load it using:

APPLOAD


Add to Startup Suite if you want it to load automatically.

🛠 Usage
1. Select objects (lines, arcs, polylines, splines).

2.Type TOTLEN in the command line.

3.Hit enter & boom!



The script will:

Calculate the total length.

Print the value in the command line.

Ask you to pick a point to place an MTEXT annotation.

Insert MTEXT with the result and correct unit.

Example output inside drawing:

Total length = 12500.00 Millimeters

⚙️ Notes

Lengths are measured in drawing database units.

The script uses INSUNITS to determine which unit name to display:

1 = Inches

2 = Feet

4 = Millimeters

6 = Meters

If the drawing is set to mm, but values are actually in meters, the script will scale automatically.

📜 License

Free to use and modify for personal or professional projects.