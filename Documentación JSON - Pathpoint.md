## Pathpoint Configuration File
  

The configuration of pathpoint is managed by a powerful JSON configuration file that let's us add and configure stages, steps, and touchpoints. The file can be uploaded and downloaded directly from the Pathpoint UI.

![structure_pathpoint](Structure_Pathpoint.png)

### Uploading a New Config File

Pathpoint offers the possibility to load the configuration file through the following option.

1. Go to the menu at the top left <br>
![Uploading1](Menu_pathpoint.png) <br>
2. Enter the option "JSON Configuration" <br>
![Uploading2](Option_configuration.png) <br>
3. Then select "Update" <br>
![Uploading3](Option_update.png) <br>
4. Locate the file you want to update and click on "open" <br>
![Uploading4](file_location.png) <br>
5. Finally the pathopint is displayed with the latest update loaded. <br>
![Uploading5](front_pathpoint.png)
<br>  

### Downloading the Currently Active Config File

Similarly, Pathpoint offers the possibility of downloading the configuration file through the following option.

1. Go to the menu at the top left <br>
![Downloading1](Menu_pathpoint.png) <br>
2. Enter the option "JSON Configuration" <br>
![Downloading2](Option_configuration.png) <br>
3. Then select the option available to download "Pathpoint_json_vX" <br>
![Downloading3](pathpoint_jason_vx.png) <br>
4. Host the file in the location you want <br>
![Downloading4](save_file.png) <br>
5. Finally the file is downloaded for your consultation <br>
![Downloading5](downloaded_file.png) <br>

### JSON Format Explained
JSON for its acronym (JavaScript Object Notation) is a data structure, whose basic function is to allow the exchange of information. Through this structure it will be possible to identify each of the elements and components that will facilitate the implementation of Pathpoint, knowing the function of its attributes, queries and data output.

#### 1. KPI
KPI by its acronym (Key Performance Indicator), are normally known as key indicators, which allow knowing the performance of a process. In the case of Pathpoint, KPIs fulfill a fundamental function, which is the measurement of specific indicators within a particular process. 

#### - Structure KPI

    "kpis": [
        	{
		    "type": 101,
		    "name": "Unique Visitors",
		    "shortName": "Unique",
		    "link": "https://onenr.io/01qwL8KPxw5",
		    "query": "SELECT count(*) as value  FROM  Public_APICall COMPARE WITH 2 day ago",
		    "value_type": "FLOAT",
		    "prefix": "$",
		    "suffix": ""
        	}
	    ]

Where:

 - ***Type***: *Defines the type of measurement to be performed, which can be: <br>
 -- "100" returns the current measurement value.  
 -- "101" returns the current value and compares it with the value of "X" previous days*
 - ***Name***: *Corresponds to the long name of the KPI.*
 - ***ShortName***: *Corresponds to the short name of the KPI.*<br><br>
 ![KPI_display](KPI2.png) <br><br>
 - ***Link***: *Corresponds to the link that directs to the KPI dashboard.*<br><br>
 ![link_KPI](linkKPI.png) <br><br>
 - ***Query***: *Corresponds to the query that is used to perform the measurement*. 
 - ***Value_type***: *It can be an integer value "INT" (example: 100) or a decimal value "FLOAT" (example: 100,2)*.<br><br>
 ![value_type](value_type_KPI.png) <br><br>
 - ***Prefix***: *It is used in the case in which you want to Identify the KPI by placing a symbol or letter at the beginning of the name. Example: USD 12000*
 - ***Suffix***: *It is used in the case where you want to Identify the KPI by adding a symbol or letter at the end of the name. Example: 5%*.
 <br><br>
 ![prefix_suffix](prefix_suffix_KPI.png) <br><br>

#### - Example KPI

![Example_KPI](Example_KPI.png)

#### - KPI Pathpoint Image

![KPI](KPI.png)

![KPI_types](KPI1.png)


#### 2. Stages  
Here you can see the business stages at a high level. For each commercial stage, different services and methods are presented at the system level. Based on business information, PathPoint previews latency indicators.
All the information related to the stage, including the errors for each one of them, allows to detail certain aspects at a high level.

#### - Structure Stage

	"stages": 
	[
           {
            "title": "BROWSE",
            "active_dotted": "none",
            "arrowMode": "FLOW",
            "percentage_above_avg": 20,
	    	"steps": 
		 [
		  "Code steps..."
		 ]
		    "touchpoints": 
			[
			   "Code touchpoints..."
			]
	   }
	 ]
	  
	  
Where:
 - ***Title***: *Corresponds to the name that identifies the stage* <br>
 ![example_titles](Examples_Titles_Stages.png)<br> 
 - ***Active_dotted***: *Defines the display of the start or end of a flow. It only handles two values: "none" or "dotted". By default it takes the value "none". When the value is changed to "dotted", it adds some dotted lines to the left of the stage where it is defined* <br>
 Here is an example when activating "dotted" <br>
 ![example_active_dotted](Example_active_dotted.png)<br>
 - ***ArrowMode***: *Defines the shape of the arrow on the header of the Stages. It only handles two values: "FLOW" and "STATIC". By default it is "FLOW"* <br>
 Example with "FLOW" <br>
 ![example_arrowMode](Example_arrowMode_flow.png)<br>
 Example with "static" <br>
 ![example_arrowMode](Example_arrowMode_static.png)<br>
 - ***Percentage_above_avg***: *Indicates the percentage that is above the mean* <br>
 ![example_percentage](Example_percentage.png)<br>

#### - Examples stage <br><br>
Example 1<br><br>
![example_stage_1](Example_Stage1.png)
<br><br>
Example 2<br><br>
![example_stage_2](Example_Stage2.png)<br><br>


#### 3. Steps
These are "sub-stages" of a main stage and represent a certain degree of granularity in your services. 

#### - Structure Steps

	"steps": [
                  {
                    "line": 1,
                    "values": 
		     [
                        {
                            "title": "Web",
                            "id": "ST1-LINE1-SS1"
                        },
                        {
                            "title": "Mobile Web",
                            "id": "ST1-LINE1-SS2"
                        },
                        {
                            "title": "App",
                            "id": "ST1-LINE1-SS3"
                        }
		     ]
		   }
                 ]

Where:
- ***Line***: *Positions the row in which the task is located within the stage.* <br>
![example_line](Examples_Line_Step.png) <br>
- ***Values***: *Indicate the parameters for each step. Currently the parameters "title" and "ID" are considered*
- ***Title***: *Corresponds to the name with which the step is identified.* <br>
![example_title](Examples_Title_Step.png) <br>
- ***ID***: *Corresponds to the code that identifies the step in its order within the row that is located. For the example, in line 1 the "Web" step is assigned the order # 1, the "Mobile Web" step has the order # 2 assigned and the "App" step is assigned the order # 3 in its configuration.* <br>
![example_id](Examples_ID_Step.png) <br>

#### - Examples Steps

Example 1<br>
![example_step_1](Example_Step1.png)
<br><br>
Example 2<br><br>
![example_step_2](Example_Step2.png)<br><br>

#### - Steps Images
When you click on any of the steps, even more detailed services and functions will be displayed in the list of associated TouchPoints. When a stage has a red border, it means that there is an error type anomaly for that stage. <br>

A step contains one or more contact points. Each step allows business stakeholders to understand the performance of the system in some way without going into all the implementation details. <br>

![steps](Steps.png)

#### 4. Touchpoints
[TBD]
  

### Different Touchpoint Types Explained

 [TBD]
  

### Example JSON Files for Different Business Sectors
- Basic E-Commerce
[TBD]
- Streaming Media
[TBD]
- Shipping & Logistics
[TBD]
- OTHER (check with Federico)
[TBD]
