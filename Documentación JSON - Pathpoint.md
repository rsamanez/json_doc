## Pathpoint Configuration File
  

The configuration of pathpoint is managed by a powerful JSON configuration file that let's us add and configure stages, steps, and touchpoints. The file can be uploaded and downloaded directly from the Pathpoint UI.

![structure_pathpoint](Structure_Pathpoint.png)

### Uploading a New Config File
[TBD]
  

### Downloading the Currently Active Config File
[TBD]

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
Aquí se pueden ver las etapas de negocio a alto nivel. Por cada etapa comercial se presentan diferentes servicios y métodos a nivel de sistema. Basado en la información comercial, PathPoint previsualiza indicadores de la latencia.
Toda la información relacionada a la etapa, incluidos los errores por cada una de ellas, permite detallar ciertos aspectos a alto nivel.

#### - Structure Stage

"stages": [
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
	  
	  
#### - Stage example

Where:
 - ***Title***: *explicar...* 
 - ***active_dotted***: *explicar...*
 - ***arrowMode***: *explicar...*
 - ***percentage_above_avg***: *explicar...*
 
 
#### - KPI Pathpoint Image ~~(imagen por verificar~~)
 
#### 3. Steps
[TBD]

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
