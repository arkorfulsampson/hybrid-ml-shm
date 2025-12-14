Inventory of Landslides Along Alabama Highways - Version 1.0 (2024)

Overview of Inventory:

This dataset provides an inventory of landslides along Alabama highways collected for different research projects led by Dr. Jack Montgomery (jmontgomery@auburn.edu). The co-authors for the current version of the landslide inventory are listed on the DesignSafe project. This inventory is based upon work funded by the Alabama Department of Transportation under grant numbers 930-931 and 931-054 and the National Science Foundation under grant number CMMI 2047402. Inclinometer data was provided by Brannon McDonald (ALDOT). Any opinions, findings, conclusions, or recommendations are those of the authors and do not necessarily reflect the views of ALDOT or the National Science Foundation. 

The current inventory contains two datasets. The first was created based on inclinometer readings collected by the Alabama Department of Transportation (ALDOT) at sites around the state. All of the inclinometers were located in areas that were previously identified as unstable and had inclinometers installed to determine the magnitude and depth of sliding. Quarterly or more frequent readings were conducted using digital inclinometer probes and the data was processed to extract the displacement at the slide plane. We filtered erroneous readings by removing readings with large changes in displacement (>2.5 mm) at the bottom of the casing, readings with spikes in displacement at a single depth without movement at other depths, and negative (upslope) displacements larger than 10 mm. The full data processing approach is described by Rahimikhameneh et al. (2024, https://rosap.ntl.bts.gov/view/dot/78284). The final inventory includes 56 inclinometers with identifiable shear zones distributed across 19 sites. The uploaded dataset contains a KML file with the location and some information about each inclinometer (see data description below) and a CSV file for each inclinometer providing the displacement readings. The columns in the CSV are described below.

The second dataset was created based on Detailed Damage Inspection Reports (DDIRs) submitted to the Federal Highway Administration (FHWA) to request federal funds for landslide repairs. DDIRs are completed for emergency relief slides where repair assistance is requested from the FHWA due to a federally declared disaster. The DDIRs provide a location, a description of the repair method, and the repair cost. While the information on each slide is limited, each report is tied to a specific initiating event (i.e., a federally declared disaster, such as a hurricane), and a complete inventory of slides is available for each event. The collection and processing of this dataset is described by Montgomery et al. (2019, https://rosap.ntl.bts.gov/view/dot/55593). The inventory of emergency relief slides contains 165 slides from 10 weather events between 2004 and 2015. The uploaded dataset is contained in a single CSV file, with each row representing a separate landslide. The columns in the CSV are described below.  

Description of Files:

1) Inclinometer-based Landslide Inventory:
This dataset consists of two types of files. The first is a KML showing the locations of each site (some sites have multiple inclinometers) and provides information about each inclinometer. The second are CSV files contained in the folder (Inclinometer Readings). Each CSV contains the processed displacement data for the inclinometer referred to in the title. A description of the data contained in each file type is below. 

- Inclinometer_Locations.kml
KML (Keyhole Markup Language) file containing points for each inclinometer. The inclinometers are grouped by site (with a single coordinate for each site), so multiple inclinometers will show as being in the same location. Each point has the following fields, which provide information about the inclinometer.
	

- CSV file for each inclinometer (e.g., AL-146 36008.csv)
Geodatabase feature class (point) for the documented landslides in the field version 1.0 (2024).
       Fields:
	o Date,
	o Slip Category: 1 - No Landslide, 2 - Uncertain, 3 - Landslide
	o Displacements (mm)
	o Change in Displacement (mm)



2) DDIR-based Landslide Inventory (2009-2015):
- ALL_DDIR.csv 
Geodatabase feature class (polygon) for the documented landslides. 
       Fields:
	o DDIR_Number: Number of the Detailed Damage Inspection Report submitted to FHWA
	o Division: ALDOT Division where the slide occurred (as of 2019)
	o County: County name where the slide occurred
	o City: City where the landslide occurred, if applicable
	o Route_Direction: Abbreviation for direction of travel lanes closest to landslide (northbound, southbound, eastbound, or westbound). All indicates that both sides were affected
	o Route_Type: Abbreviation for route type: State route (SR), US Highway (US), Interstate (I), or County Road (CR)
	o Route_Number: Number of road
	o Ramp_Int: Description of ramp type for slides that occurred on onramp/offramps or interchanges
	o Road_Discript: Further description of location or roadway, if applicable
	o MP: Nearest milepost for point features
	o MP_Start: Nearest milepost to start of line features
	o MP_End: Nearest milepost to end of line features
	o Lat: Latitude for point features
	o Long_: Longitude for point features
	o Lat_Start: Latitude at start of line features
	o Lat_end: Latitude at end of line features
	o Long_Start: Longitude at start of line features
	o Long_end: Longitude at start of line features
	o Event_Year: Year of landslide
	o Failure_Event: Name assigned to initiating event for this inventory
	o Weather: Classification for type of event: Rain, Flooding, Tornados, Hurricane
	o Front_Back: Location of slide on roadway as either the front slope (slope with a negative grade when moving away from the centerline of the roadway) or back slope (slope with a positive grade when moving away from the centerline of the roadway). 
	o Repair_Cost: Estimate of repair costs from DDIR
	o Repairs: Description of repair approach if available	
	o Repair_Type: Repair type as either emergency (E), permanent (P), or both (E/P)
	o InspectionDate: Date of inspection of the landslide
	o Failure_Discript: Description of the landslide provided on DDIR
	o Severity: Impacts of slide on roadway
	o Failure_Type: Classification of type of failure based on categories described in Chapter 2.3 of Montgomery et al. (2019)
	o Shallow_Deep: Classification of slip surface as either shallow (exiting at or above toe of slope) or deep (extending below toe of slope) 
	o Addition_Comment: Any additional comments from DDIR
	o FHWA _Disaster_No: Disaster number assigned to the initiating event

