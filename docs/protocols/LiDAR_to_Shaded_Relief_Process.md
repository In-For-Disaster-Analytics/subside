**LiDAR to Shaded Relief – Process Steps**

1.  Prepare the workspace:

    1.  Create these folders: **LAS, LAS_Datasets**

    2.  Create these geodatabases: **DEMs.gdb, Merged_DEMs.gdb, Mosaic.gdb**

2.  Determine the necessary LiDAR las files

    1.  Download the TNRIS LiDAR Availability Index: <https://tnris.org/data-download/#!/statewide> (Tnris-lidar_tx.zip)

    2.  Overlay the lidar index with the quarter quad index and other reference layers to determine the name of the acquisition (i.e. – CAPCOG 2007 140cm LiDAR), the las filenames, and the quarter quads that need to be downloaded.

    3.  **Important:** Ensure the selected las grids create a complete rectangle. If you have an irregular set of grids, the resulting DEM below will be distorted
<figure markdown="span">
  ![Correct](images/LiDAR_to_Shaded_Relief_Process/image1.png){ width="300" }
  <figcaption>Correct</figcaption>
</figure>
<figure markdown="span">
  ![Incorrect](images/LiDAR_to_Shaded_Relief_Process/image2.png){ width="300" }
  <figcaption>Incorrect</figcaption>
</figure>

3.  Download the LiDAR las files from TNRIS

    1.  Link: <https://tnris.org/data-catalog/>

    2.  Click the lidar filter

    3.  Click the A-Z button to put into alphabetic order (easier to locate the acquisition name)

    4.  Click the acquisition you want

    5.  Click the **Launch Data Search and Download** button.

    6.  Type in the the name of the quad and select the correct one from the dropdown list. Since you already have the quad name, it is not necessary to enter a county.

    7.  Scroll down to the LiDAR and Derived Products

    8.  Download the correct quarter quad for the acquisiiton you are interested in.

    9.  Save this to the LAS folder you created above.

4.  Import the LAS files

    1.  Uncompress the LiDAR zip file

    2.  If you haven’t already done so, download and install the [LASZip software](https://laszip.org/).

    3.  Go into the downloaded las subfolder and use LASZip to unzip the las files you need. You can either right click and Open With... or you can drag and drop the las file on top of the LASZip desktop icon.

5.  Create LAS Dataset:

    1.  Open ArcPro and open the **Create LAS Dataset** tool

    2.  Select the input LAS files

    3.  Save the output to the LAS_Datasets folder

    4.  For coordinate system, import from one of the las files to ensure its using the source’s projection.

    5.  Hit Run

    6.  Review the new LAS dataset on the map to ensure it is falling into the right place. If it does not, the projection information is not defined. In these cases, use the **Define Projection** tool to create prj files for each las.

6.  Create DEMs from LAS dataset

    1.  Open the **LAS Dataset to Raster** tool.

    2.  Select the input LAS Dataset

    3.  For Output, save the file to DEMs.gdb adding the suffix \_DEM to the name.

    4.  Set the sampling rate (For 140cm – 1.2, For 50cm - .4, For 100cm - .9)

    5.  Run

7.  Create Hillshade

    1.  Open the Hillshade (Spatial Analyst) tool

    2.  For Input, Select the DEM just created.

    3.  For Output, save to ***DEMs.gbd*** adding the suffix \_HS to the name.

8.  Create an Mosaic Dataset (empty for now)

    1.  Open the **Create Mosaic Dataset** tool.

    2.  For Output, save it to ***Mosaic.gdb***, giving it the name of the area and a \_Mosaic suffix.

    3.  Import the projection from a source las file or your LAS Dataset.

9.  Add Rasters to the Mosaic

    1.  Navigate to the new Mosaic in Catalog

    2.  Right-click on it and select **Add Rasters**

    3.  For Input Data, select **Dataset**

    4.  Add the each of the DEMs created from the LAS Datasets (Remember, these should form a complete rectangle or the final image will be distorted)

    5.  Under Raster Processing, check the boxes for Calulate Statistics and Build Raster Pyramids

    6.  Under Mosaic Processing, check Build Thumnails, Update Overviews, and Estimate Mosaic Dataset Statistics

    7.  Hit Run

10. Create Merged DEM from Mosaic

    1.  Open the new mosaic in the map

    2.  Right-click and Export to Raster. Save this in Merged_DEMs.gdb

11. Create final Shaded Relief

    1.  Add new merged DEM to a map

    2.  With the mosaic selected, go to the appearance tab. For Resampling Type, select cubic.

    3.  Set symbology

        1.  Right-click the mosaic and open the symbology interface.

        2.  For Color Scheme, select Bathymetric Scale (purple to red)

        3.  For Stretch Type, select Standard Deviation

    4.  Add Hillshades

        1.  Add all of the hillshades to the map, placing them above the mosaic. Alternatively, these hillshades could be pulled into their own mosaic, but is not required when publishing a service.

        2.  While on the Apppearance tab, select each hillshade and set the transparency to 48%.

12. Publish service

    1.  Go to the Share tab

    2.  Web Layer: Publish Web Layer

    3.  For Name, include the name of the area with a suffix of \_ShadedRelief

    4.  Provide Summary and tags

    5.  Leave Data and Layer Type at default settings (Map image)

    6.  Set the output folder and share information

    7.  Publish
