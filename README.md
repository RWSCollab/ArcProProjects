# ArcProProjects
Below is the workflow to publish a service to the MGEL Enterprise Portal for the RWSC Portal.

## Samantha's side 
- Create an ArcGIS Pro project (.aprx). 
  - Can contain multiple maps. All the maps in the project will be published as separate weblayers. 
  - The map name (title) has to be the service name. Letter cases, spaces, underscores, etc matter. Do not include version numbers. The spaces in the map name will be replaced with dashes "-".
    - e.g., The map title "Passive Acoustic Monitoring" will become the service name "Passive_Acoustic_Monitoring". 
  - Can contain basemap though the basemap will not be included in the service. 
  - Make sure all data sources are local (e.g. file geodatabase, shapefile). No data from the enterprise geodatabase should be included. 
  - Make sure the visibility of the layers (the groups and layers are checked or unchecked) is managed according to what you expect when the service is initially loaded online. 
  - The metadata should be entered in the map & layers’ metadata section. The summary, tags, description, credits and use limitations of the map metadata will be used for the service metadata.
- Package the project using the “Package project” tool.
  - Output file name should be the same as the map title.
  - Check "All versions" for the Package Version.
  - Uncheck "Include Toolboxes". 
- Upload the package (.ppkx) to the GitHub repository at https://github.com/RWSCollab/ArcProProjects 
- Notify the MGEL team. 

## MGEL's side 
- Download the package and load it with ArcGIS Pro.
  - Downloaded package is saved in V:\GIS_Phase2\RWSC RPT\RWSC_Samantha
  - The package is unpacked in V:\GIS_Phase2\RWSC RPT\RWSC_Samantha\unpacked. This is a temporary folder. Every time the script is executed, this folder is first cleared.
- Publish it to the Enterprise Portal. 
  - Folder: RWSC 
  - Categories: RWSC 
  - Group: RWSC 
  - Share level: Public
 
  All the steps above are done by a Python script under seamap-arcgispro-gee repo - DensityModels/MDAT/UploadToPortal.py. Please read the notes in the script carefully before running it.
