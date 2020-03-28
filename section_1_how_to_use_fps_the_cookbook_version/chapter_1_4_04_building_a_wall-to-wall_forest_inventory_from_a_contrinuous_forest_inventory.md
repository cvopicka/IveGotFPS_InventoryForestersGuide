# Chapter 1.4.04 - Building a Wall-to-Wall Forest Inventory from a Continuous Forest Inventory (CFI)[^5]

- Open a Blank FPS Database[^6]
- Enter/Import Your Admin Data (polygons)
- **Update FPS from GIS**
  - *Editors*
  - *Update FPS from "GIS VegPoly"*
    - *Import Flags, GIS_Lbl and Theme from GIS VegPoly*
    - *Import Xgis and Ygis from GIS VegPoly*
    - *Import Gross, Net and Report Acres from GIS*
- Enter / Import CFI Data
  - Assign each plot to the stand it falls within. Typically using the plot number for the plot number and the stand number of the stand it falls within as the stand number.
- **Compile Cruised Stands**
  - *Selection*
    - *Select All Stands*
  - *Compiler*
    - *Run Cruise Compiler*
      - *Select No Options*
      - *Start*
- **Update Physical Site for ALL Stands**
  - *Selection*
    - *Select All Stands*
  - Link SiteGrid[^7]
  - *Editors*
    - *Update Physical Site from SiteGrid*
      - *Update Admin from average of SiteGrid points within polygon (Admin.Flag > 0)*
      - *Start*
- ***Create new Habitat/Report Classification\utility on all cruised stands.***
  - *Selection*
    - *Select No Stands*
    - *Add Cruised Stands*
  - *Strata*
    - *Create new Habitat/Report Classification*
      - *Start*
- **Grow the cruised stands to the current year.**
  - *Selection*
    - *Select No Stands*
    - *Add Cruised Stands*
  - *Growth*
    - *Build/Edit/Switch Silvics Regime*
      - Navigate to Origin regime (NATR / PLNT)
      - *Assign as an Existing Inventory Regime*
      - *Save updates and Close*
  - *Growth*
    - *Build/Edit/Switch Silvics Regime*
      - Navigate to Growth regime (GROW)
      - *Assign as a Future Planning Regime*
      - *Save updates and Close*
    - *Grow Stands*
      - *Grow to*: at minimum pick the largest common year or pick this year
      - *Grow All Tables*
      - *Start*
- ***Run Cruise Expansion on Veg_Lbl***
  - *Selection*
    - *Select All Stands* (if a large dataset you may need to divide into sections)
  - *Strata*
    - *Run Cruise Expansion on Veg_Lbl*
      - *Expand All Tables from cruised stands (within each Veg_Lbl type).*
      - *Start*
- ***Create new Habitat/Report Classification\utility* on all stands.**
  - *Selection*
    - *Select All Stands*
  - *Strata*
    - *Create new Habitat/Report Classification*
      - *Start*
- **Run Reports**

__WARNING__

CFI inventories were not designed to do this extrapolation. Use at your own risk. If it is all you have to start with you must move to a stand based sampling methodology.

[^5]:See the appropriate chapters for more detailed information.
[^6]:It is suggested that all organizations maintain a blank customized FPS database.
[^7]:See chapter on linking & importing data
