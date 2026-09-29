# Conveyor Game

**Beltline Fabricator** is a browser sandbox game about building conveyor lines.

Lay out frames, fit rollers and belts, bolt on drive motors, and ship cartons from the infeed to the shipping bin while staying on budget.

## Play

Open `index.html` in any modern browser. There's no build step and nothing to install.

## Controls

| Input | Action |
| --- | --- |
| Drag with Frame / Full section | Lay a run in the drag direction |
| `1`–`7` | Frame, Rollers, Belt, Drive motor, Full section, Remove, Inspect |
| `Q` `W` `E` `A` `S` `D` `F` | Twin trough, Flights, Hopper, Cover, Twin drive, Spout, Saddle foot (screw feeder orders) |
| `R` | Rotate |
| Right-click | Remove a section (parts are refunded) |
| Space | Pause / run |

## How a section works

Each 1 m section needs a **frame**, **rollers**, and a **belt**. A **drive motor** powers up to 6 m of connected belt. The belt runs at 1 m/s, and each section holds one carton at a time.

## Work orders

1. **First run**: a straight line from the infeed to the bin.
2. **Around the columns**: route around building columns.
3. **Two lines, one dock**: merge two infeeds into one bin.
4. **Sample blueprint: twin screw feeder**: build 2 units to print, then discharge 40 scoops.
5. **Open shop floor**: a sandbox with every part, where you place your own infeeds and bins.

## Add a blueprint

Press **Add blueprint** to turn a drawing into a work order you can build.

1. Choose a drawing, as a PDF or an image. For a PDF, the game reads the title block and notes to fill in the spec: diameter and overall length (`14" DIA X 20'-0" LG TWIN FEEDER`), units required (`QTY REQ'D: 02 UNITS`), hopper size (`20 CU YD HOPPER`), and flight pitch zones (`14" DIA X 5" PITCH ... 90" LG`).
2. Check the spec and fix anything it missed: name, type (screw or belt), twin screws, overall length, units (up to 3), hopper length and flight pitch zones.
3. Press **Create work order**. The game lays a blue outline on the floor with one 1 m section per 3.3 ft of length, and a checklist that verifies each unit against the print.

Blueprints and drawings are kept in your browser only. Nothing is uploaded. **View drawing** reopens the sheet while you build, and **Remove blueprint** deletes it. The PDF reader (pdf.js) loads from cdnjs the first time you open a PDF.

### Screw feeder blueprints

Each section is built as **trough → flights → hopper or cover**. The **screw drive** goes on the inlet end, the **discharge spout** on the far end, and **saddle feet** on the middle sections. Flight pitch sets screw speed (0.08 m/s per inch of pitch, so 5" moves 0.4 m/s and 14" moves 1.1 m/s), which is why feeders open the pitch toward the discharge. Loaders can only dump into a hopper. The order closes once every unit passes the built-to-print check and the quota is discharged.

### Belt conveyor blueprints

Each section needs a frame, rollers and a belt, plus a drive motor on every section the outline marks (one per 6 m).
