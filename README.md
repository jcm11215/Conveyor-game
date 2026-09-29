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
4. **Blueprint: twin screw feeder**: build 2 units to print (see below), then discharge 40 scoops.
5. **Open shop floor**: a sandbox with every part, where you place your own infeeds and bins.

## Blueprint: twin screw feeder

Based on a fabrication print for a 14" dia × 20'-0" twin screw feeder with a 20 yd³ hopper, 2 units required. Each grid section is about 1 m, so one unit is 6 sections along the blue outline:

| Section | Top | Flight pitch | Extra |
| --- | --- | --- | --- |
| 1 | Hopper | 5" | Twin drive (two gearmotors, one per screw) |
| 2 | Hopper | 5" | |
| 3 | Hopper | 7" | |
| 4 | Hopper | 7" | |
| 5 | Cover | 7" | |
| 6 | Cover | 14" | Discharge spout |

Build each section as **twin trough → LH/RH flights → hopper or cover**. Add **3 saddle feet** per unit on the middle sections (the trough ends stand on their own feet). Flight pitch sets screw speed (5" 0.40 m/s, 7" 0.55 m/s, 14" 1.1 m/s), which is why the print opens up the pitch toward the discharge. Loaders can only dump into a hopper. The order closes once both units pass the built-to-print check and 40 scoops have been discharged.
