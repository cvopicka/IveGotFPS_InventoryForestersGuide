# Chapter 2.3.01 - Building a Wall-to-Wall Forest Inventory

- Open a Blank FPS Database
- Enter/Import Your Admin Data (polygons)

FPS is designed to be a forest level management tool as such FPS must know all stands or polygons. To do this it will be required that you enter a minimum amount of information in the ADMIN table. All stands must have a unique Std_ID at minimum. Typically this is the same as the GIS_ID in the admin table that is used to link FPS and GIS. This is the bare minimum required as the next step will import the information from GIS.

It is recommended that ALL polygons of a given ownership be put in to the FPS database. Just because something is not productive now or an RMA doesn't mean that later it will be the same. Plus the added bonus that some of those acres may count towards the ownership objectives and regulatory constraints.

This step assumes that you will be linking or importing your VegPoly from GIS for the next step to work.

- *Update* FPS from GIS
  - *Editors*
    - *Update FPS from "GIS VegPoly"*
    - *Import Flags, GIS_Lbl and Theme from GIS VegPoly*
    - *Import Xgis and Ygis from GIS VegPoly*
    - *Import Gross, Net and Report Acres from GIS*

While this is not truly a required step it can be helpful so that the user need not enter all the information manually. All this process will do is copy data with matching GIS_ID values from the VegPoly to the ADMIN table. For this to work it is necessary to have a properly formatted VegPoly. One nice trick here is that you can link any of your compatible GIS files and rename the link in MS Access. The link name will not change the name of the linked table.

- **Collect Data / Cruise the Forest**
  - *Selection*
    - *Select All Stands*
  - *Compiler*
    - *Run Cruise Selection*
    - Set *% of Area to be Sampled* = 20
    - *Start*

Where to sample? This step is just a guide to help determine where to sample. The above are arbitrary targets but a good starting point. The cruise selection routine works by Veg_Lbl and samples with a probability proportional to size method. What this means is that you will get a suggested 20% sample (usually a little more) for each Veg_Lbl and larger stands will be selected to sample over smaller stands. More on this exact calculation in the next chapter.

- Enter / Import Cruise Data

This method will vary based on your data source and collection methods.

- **Compile Cruised Stands**
  - *Selection*
    - *Select All Stands*
  - *Compiler*
    - *Run Cruise Compiler*
    - Select No Options
    - *Start*

Now that I have sampled stands what do I have? The cruise compiler will take your tree data and mix it with your cruise design and create a summarized output of your sampled data.

- **Update Physical Site for ALL Stands**
  - *Selection*
    - *Select All Stands*
  - Link SiteGrid
  - *Editors*
    - *Update Physical Site from SiteGrid*
    - *Update Admin from average of SiteGrid points within polygon (Admin.Flag > 0)*
    - *Start*

This may be optional. For FPS to project data in to the future this is required. But this only needs to be done once per polygon update. This means that initially this will have to be run to apply a site index and site shape to all stands. After this initial assignment it will be necessary to update stands when stand boundaries are updated.

- ***Create new Habitat/Report Classification* utility on all cruised stands.**
  - *Selection*
    - *Select No Stands*
    - *Add Cruised Stands*
  - *Strata*
    - *Create new Habitat/Report Classification*
    - *Start*

Creating a new habitat classification allows for natural regeneration and reports to be run.

- **Grow the cruised stands to the current year.**
  - *Selection*
    - *Select No Stands*
    - *Add Cruised Stands*
  - *Growth*
    - *Build/Edit/Switch Silvics Regime*
      - Navigate to Origin regime (NATR / PLNT)
      - *Assign as an Existing Inventory Regime*
      - *Save updates and Close*
      - Navigate to Growth regime (GROW)
      - *Assign as a Future Planning Regime*
      - *Save updates and Close*
    - *Grow Stands*
      - *Grow to*: at minimum pick the largest common year or pick this year
      - *Grow All Tables*
      - *Start*

Bringing the cruised stands to a common year. This is important because all stands need to be in a common state before they can be aggregated for expansion. If all of the stands of a given VEG_LBL are in different years they will not effectively represent the current / common status of that VEG_LBL.

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
