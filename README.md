# ArcProProjects
Below is the workflow to publish a service to the MGEL Enterprise Portal for the RWSC Portal.

## Samantha's side 
- Create an ArcGIS Pro project (.aprx). 
  - Can contain multiple maps. All the maps in the project will be published as separate weblayers. 
  - The map name (title) has to be the service name. Letter cases, underscores, etc matter. Do not use space. Do not include version numbers.  
  - Can contain basemap though the basemap will not be included in the service. 
  - Make sure all data sources are local (e.g. file geodatabase, shapefile). No data from the enterprise geodatabase should be included. 
  - Make sure the visibility of the layers (the groups and layers are checked or unchecked) is managed according to what you expect when the service is initially loaded online. 
  - The metadata should be entered in the map & layers’ metadata section.
- Package the project using the “Package project” tool. 
- Upload the package (.ppkx) to the GitHub repository at https://github.com/RWSCollab/ArcProProjects 
- Notify the MGEL team. 

## MGEL's side 
- Download the package and load it with ArcGIS Pro. 
- Publish it to the Enterprise Portal. 
  - Folder: RWSC 
  - Categories: RWSC 
  - Group: RWSC 
  - Share level: Public 
