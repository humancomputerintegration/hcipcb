# hcipcb

KiCAD library with custom parts for [CMSC 23230/33230: Engineering Interactive Electronics onto Printed Circuit Boards](http://hcipcb.plopes.org/) at the University of Chicago

## Setup

Clone this repository:

```
git clone https://github.com/humancomputerintegration/hcipcb.git
```

### 1. configure library path

1. In the main window of KiCAD, go to **Preferences > Configure Paths**
2. **Create a new environmental variable** (+ button on bottom-left) with the **name `HCIPCB_LIB`** and **path as the `hcipcb` directory** (e.g. `/Users/username/hcipcb`). This helps load the 3D models for footprints.

### 2. add symbol library (.kicad_sym)

1. In the main window of KiCAD, go to **Preferences > Manage Symbol Libraries > Global Libraries tab**
2. Click **Add empty row to table** (plus icon near the bottom)
3. Add `hcipcb` for the **Nickname** and `${HCIPCB_LIB}/hcipcb.kicad_sym` for the **Library Path**

### 3. add footprint library (.pretty folder)

1. In the main window of KiCAD, go to **Preferences > Manage Footprint Libraries > Global Libraries tab**
2. Click **Add existing library to table** (same icon as with Symbol Libraries)
3. Add `hcipcb` for the **Nickname** and `${HCIPCB_LIB}/hcipcb.pretty` for the **Library Path**

## Verifying set up

1. **Open a new schematic** (`.sch`) file or re-open an existing one
2. **Add a new symbol** (Place > Place Symbol > click on schematic)
3. You should see **hcipcb** as a new category. To make it easier for the future, you can right click and **Pin Library** so it always appear on top. **Place the USB4105-GF-A** onto the schematic. This is the USB connector we'll be using. Annotate it as "J1".
4. Go to **Tools > Update PCB from Schematic**, and place the USB4105-GF-A footprint onto the board.
5. Ensure the 3D model for the USB connector is loaded by going to **View > 3D Viewer** (selected model will turn green)

## Questions?

Email us at the helpdesk (email linked in the class wiki)!
