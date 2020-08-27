# ESS-DIVE Sample ID and Metadata Guide

Here you will find proposed guidelines for standardizing sample metadata to describe interdisciplinary samples within DOE's Environmental Systems Science community.

ESS-DIVE recommends obtaining International General Sample Numbers (IGSNs) for samples from the System for Earth Sample Registration (SESAR). Most of this proposed sample standard follows [SESAR's metadata guidelines](http://doi.org/10.5281/zenodo.3874923). However, we have proposed changes to metadata elements, specific requirements, and vocabularies based on ESS community needs. 

We seek any additional feedback, with the goal of making ESS sample information **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable (FAIR). 

---  
**Sample Metadata**

- [Header Rows](#header-rows)
  * [Object Type](#object-type)
  * [User Code](#user-code)
- [Sample IDs and Related Identifiers](#sample-ids-and-related-identifiers)
  * [Sample Name](#sample-name)
  * [Other name(s)](#other-name-s-)
  * [IGSN](#igsn)
  * [Parent IGSN](#parent-igsn)
  * [Collection ID](#collection-id)
  * [Event ID](#event-id)
  * [Site ID](#site-id)
- [Sample Description](#sample-description)
- [Sample Collection Details](#sample-collection-details)
- [Location](#location)
- [Environmental Context](#environmental-context)
- [Sample Access](#sample-access)


---  

## Header Rows

### Object Type
|ESS-DIVE Proposed Element|objectType <code>Required</code>                     | 
|:------------------------|:----------------------------------------------------|
|**Format**               |[Controlled list](https://www.geosamples.org/help/vocabularies#object)|
|**Definition**           |Broad characterization of the nature of a sample or specimen.|
|**Additional Instructions**|See [object type crosswalk](https://github.com/ess-dive-community/sample-id-metadata/blob/master/objectType.md) for revised terms <br>proposed for ESS-DIVE, and provide feedback on additional terms or revisions needed.
|**Examples**             |Core; Individual Sample; Organism|

### User Code 
|ESS-DIVE Proposed Element|userCode <code>Required</code>                       |
|:------------------------|:----------------------------------------------------|
|**Format**               |Five-letter code                                     |
|**Definition**           |Globally unique IGSN code that will be used as a prefix <br>for IGSNs in the submitted batch template.|
|**Additional Instructions**|User codes should be unique to an individual or large project managed by a team;<br> avoid creating multiple user codes. If assigning IGSNs in the IGSN column, <br>the user code must match the user code in the IGSNs. For example, if the user <br>specifies IEMEG is the user code, any user-specified IGSNs must begin with IEMEG.<br> If you do not specify the user code to be used, a default user code belonging<br> to the registrant will be used.|
|**Examples**             |IEMEG, IEJDE                                        |

---  

## Sample IDs and Related Identifiers

### Sample Name
|ESS-DIVE Proposed Element|sampleName <code>Required</code>                     |
|:------------------------|:----------------------------------------------------|
|**Format**               |free text, unique                                    |
|**Definition**           |Collector's project-specific sample name, which must be unique for each sample that<br> you are submitting.|
|**Additional Instructions**|You can develop a sample ID that has meaning to you and may help in your internal, <br>project sample management.|
|**Examples**             |001-ER18-FO                                          |

### Other name(s) 
|ESS-DIVE Proposed Element|otherName <code> Optional </code> <img width=400/>   |
|:------------------------|:----------------------------------------------------|
|**Definition**           |Other sample name(s) that have been used in the past.|
|**Format**               |free text                                            |
|**Additional Instructions**|Use a semi-colon to delimit multiple names where needed.|
|**Examples**             |001ER18FO; 001ER18-FO                                |

### IGSN
|ESS-DIVE Proposed Element|IGSN <code> Recommended </code>                      |
|:------------------------|:----------------------------------------------------|
|**Definition**           |Globally unique and persistent identifier for the sample. Leave blank if you want <br>SESAR to assign the IGSN, which is recommended.|
|**Format**               |semi-opaque, alphanumeric characters (9 recommended) |
|**Additional Instructions**|For split samples/subsamples, you can assign your own 1-2 character extensions from <br> the Parent IGSN, and submit your own IGSNs for registering these child samples.<br>  This is not required, but is an option if desired. For assigning your own <br>IGSNS, you must use <br>upper-case alpha-numeric characters.|
|**Examples**             |IEWER7214, IEMEG0215                                 |

### Parent IGSN 
|Proposed ESS-DIVE Element|parentIGSN <code>Required</code>, if relevant        |
|:------------------------|:----------------------------------------------------|
|**Definition**           |The larger sample from which a child sample was derived. For example, a core<br> section may be the parent of a series of subsamples or split samples.<br> Parent and child samples are linked in the SESAR catalog. Sibling samples are<br> inferred from parent-child relationships and are linked on the landing page<br> for a sample.    |
|**Format**               |semi-opaque, alphanumeric characters (9 recommended) |  |**Additional Instructions**|Leave blank if a parent IGSN does not exist.       |
|**Examples**              |IEMEG0002                                           |

### Collection ID 
|Proposed ESS-DIVE Element|collectionID <code>Optional</code>                   |
|:------------------------|:----------------------------------------------------|
|**Definition**           |A unique identifier for the set of information associated with a collection<br> of samples; collections may be organized around a particular project, data set,<br> field season, region, site, etc. |
|**Format**               |free text, unique                                    |
|**Additional Instructions**|Not in SESAR. Must be unique within the data package (project-assigned, and does<br> not need to be globally unique). See link to diagram that demonstrates <br>linking related collection, site, event, and sample IDs. A collection identifier<br> can be used to link a set of samples together, and/or to enable efficient<br> entry of metadata that is the same across all samples in a "sample collection."|
|**Examples**             |WSFA_June2019                                        |

### Event ID 
|Proposed ESS-DIVE Element|eventID <code>Optional</code>                        |
|:------------------------|:----------------------------------------------------|
|**Definition**           |A unique identifier for the set of information associated with an Event <br>(something that occurs at a place and time).|
|**Format**               |free text, unique                                    |
|**Additional Instructions**|Not in SESAR. Must be unique within the data package (project-assigned, and does<br> not need to be globally unique). See link to diagram that demonstrates<br> linking related collection, site, event, and sample IDs. An event identifier<br> can be used to link a set of samples collected on a specific date,  and/or to<br> enable efficient entry of metadata that is the same across these samples.|
|**Examples**             |WSFA_20191023                                        |

### Site ID
|Proposed ESS-DIVE Element Name       |siteID <code>Optional</code>                        |
|:------------------------------------|:---------------------------------------------------|
|**Definition**                       |A unique identifier for the set of site location information. May be a global unique identifier or an identifier specific to the data set.|
|**Format**                           |free text, unique                                   |
|**Additional Instructions**          |Not in SESAR. Must be unique within the data package (project-assigned, and does not need to be globally unique). See link to diagram that demonstrates linking related collection, site, event, and sample IDs. A site identifier can be used to link a set of samples collected from a specific site,  and/or to enable efficient entry of metadata that is the same across these samples. |
|**Examples**                         |CoyoteRiver_D22                                     |

---  

## Sample Description

### Material 
|Proposed ESS-DIVE Element Name       |material<code>Required</code>        |
|:------------------------------------|:------------------------------------|
|**Definition**                       |Material that the sample consists of.|
|**Format**                           |[Controlled list](https://app.geosamples.org/reference/materials.php)
|**Additional Instructions**          |ESS-DIVE is requesting additional terms for organisms, organic material, and water samples. [See ESS-DIVE proposed material terms, and provide feedback on modifications needed.](https://github.com/ess-dive-community/sample-id-metadata/blob/master/material.md) |
|**Examples**                         |soil; sediment; surface water [ENVO:00002042](http://purl.obolibrary.org/obo/ENVO_00002042); groundwater [ENVO:01001004](http://purl.obolibrary.org/obo/ENVO_01001004) |


### Field name (informal classification) 
|Proposed ESS-DIVE Element Name       |classification, or remove <code>Optional</code>                   |
|:------------------------------------|:-----------------------------------------------------------------|
|**Definition**                       |Informal classification of sample                                 |
|**Format**                           |free text                                                         |
|**Additional Instructions**          |Here you can add additional material classifications that are not in the current SESAR IGSN controlled fields.  We will remove this field when object-type and material controlled terms are revised and expanded to accomodate ESS sample types.  |
|**Examples**                         |leaf, root                                                        |

### Sample Description 
|Proposed ESS-DIVE Element Name       |sampleDescription <code>Recommended</code>|
|:------------------------------------|:-----------------------------------------|
|**Definition**                       |Description of sample features, such as its components, texture, color, shape, treatments, plot ID from which the sample was taken, etc.|
|**Format**                           |free-text                                 |
|**Additional Instructions**          |                                          |
|**Examples**                         |Example 1) Day 223 core section from unheated control plot 1C of a deep soil warming experiment; Example 2) Filter used for filtered surface water samples|

### Purpose                           
|Proposed ESS-DIVE Element Name       |purpose <code>Recommended</code>                  |
|:------------------------------------|:-------------------------------------------------|
|**Definition**                       |The scientific purpose for collecting the sample. |
|**Format**                           |free text
|**Additional Instructions**          |Purpose may often be the same across a series/collection of samples; To avoid entering the same information across numerous samples, you can create a separate file with metadata to describe a sample collection, which contains a "collectionID", and any associated metadata fields (e.g. "collectionMethodDescription", "Purpose", "Chief Scientist", etc.). |
|**Examples**                         |Characterize the biogeochemistry, geochemistry and microbiology of soils associated with trees and shrubs. |

|Size|<code>Optional</code>|
|:---|:---|
|Proposed Element Name|size|
|Example|4; 6.8|
|Definition|Size of the registered object, such as the surface area, length of a core, weight, or volume|
|Additional Instructions|| Must be associated with Size unit. 

|Size unit|<code>Optional</code>, <code>Required</code> if Size is provided|
|:---|:---|
|Proposed Element Name|sizeUnit|
|Example|square centimeter; kilogram|
|Definition|Unit for the numerical value provided for ‘size’.|
|Additional Instructions|Choose unit terms from the [controlled list](https://docs.google.com/spreadsheets/d/1FJ08qEM9ZTY_V6hPMcpbwYud0s8h6AV_RbuWGcuxtHU/edit#gid=0).|

|Filter Size|<code>Required</code>, if object type is "fitrate" or "material captured in filter"|
|:---|:---|
|Proposed Element Name|filterSize|
|Example|0-0.22 micrometer|
|Definition|Filtering pore size used in sample preparation (filter size value range). Filter size value range (float-float unit).|
|Additional Instructions||

|Scientific Name|<code>Required</code>, if object type is "organism"|
|:---|:---|
|Proposed Element Name|scientificName|
|Example|Vochysia ferruginea; Miconia borealis; Terminalia amazonia|
|Definition|The full scientific name, with authorship and date information if known. When forming part of an Identification, this should be the name in lowest level taxonomic rank that can be determined.|
|Additional_instructions||

|Sample Remarks|<code>Optional</code>
|:---|:---|
|Proposed Element Name|sampleRemarks|
|Example||
|Definition|Comments or notes about the sample. |
|Additional Instructions|Free text. You can include weather descriptions here, if relevant |

---

## Sample Collection Details

|Collector/Chief Scientist|<code>Required</code>|
|:---|:---|
|Proposed Element Name|collector|
|Example|John Smith|
|Definition|Name of the person(s) who collected the sample.|
|Additional Instructions|You can enter multiple collectors/sampling team for large sampling efforts, separated with a semi-colon. If the collector(s) of the sample(s) is/are not known, enter name of the person responsible for the sample.|

|Collection Date|<code>Required</code>|
|:---|:---|
|Proposed Element Name|collectionDate|
|Example|2019-08-14|
|Definition|Date when the sample was collected. YYYY-MM-DD|
|Additional Instructions|All dates and times must be reported in Coordinated Universal Time (UTC) and follow the ISO 8601 standard (RFC 3339). Temporal data using different standards can be provided as a separate variable (column) in addition to UTC format.|

|Collection Time|<code>Optional</code>|
|:---|:---|
|Proposed Element Name|collectionTime|
|Example|12:05:03Z|
|Definition|Time when the sample was collected. HH:MM:SSZ|
|Additional Instructions|All dates and times must be reported in Coordinated Universal Time (UTC) and follow the ISO 8601 standard (RFC 3339). Temporal data using different standards can be provided as a separate variable (column) in addition to UTC format.|

|Collection Method Description|<code>Required</code>
|:---|:---|
|Proposed Element Name|collectionMethodDescription|
|Example|Example 1) Collect soil samples from top 10 cm using 2-3 cores from with meadow plot or under the bulk of tree/shrub canopies.  Example 2) Excised branch. Example 3) Pumped water at specific depths using tubing connected to CTD.|
|Definition|Description of the collection method for the sample. Include any important terms and details for potential users to understand how your sample was collected.|
|Additional Instructions|Collection methods may often be the same across a series/collection of samples; there are two options for providing collection method details at a higher level. Option 1:  Create a separate file with metadata to describe a sample collection, which contains a "collectionID", and any associated metadata fields (e.g. "collectionMethodDescription", "Purpose", "Chief Scientist", etc.).  Option 2: Create a methods file, with a series of methods descriptions that are each associated with a "methodID" and an associated "methodDescription." |

|Sample Processing|<code>Recommended</code>, if relevant. Not in SESAR|
|:---|:---|
|Proposed Element Name|sampleProcessing|
|Example|filter water; store samples in ethanol|
|Definition|Any processing applied to the sample during or after retrieving the sample from the environment. Can provide a list of preparations and preservation methods for the sample.|
|Additional Instructions|Sample processing may often be the same across a series/collection of samples. To avoid entering the same information across numerous samples, you can create a separate file with metadata to describe a sample collection, which contains a "collectionID", and any associated metadata fields (e.g. "sampleProcessing", "collectionMethodDescription", "Purpose", "Chief Scientist", etc.). Separate multiple sample processing methods with a semi-colon.|

|Field program/Cruise|<code>Optional</code>, <code>Required</code> at package level, but want to associate with samples for data search and integration.|
|:---|:---|
|Proposed Element Name|projectName|
|Example|Next Generation Ecosystem Experiments (NGEE) Tropics; LBNL Watershed Function SFA |
|Definition|Enter the name of the DOE project to associate with this/these sample(s).|
|Additional Instructions|If multiple projects were involved, enter the project that had the largest contribution first, and separate entries with a semi-colon. Project Name may often be the same across a series/collection of samples; To avoid entering the same information across numerous samples, you can create a separate file with metadata to describe a sample collection, which contains a "collectionID", and any associated metadata fields (e.g. "Project Name", "collectionMethodDescription", "Purpose", "Chief Scientist", etc.).|

---  

## Location  

|Latitude (Coordinate system: WGS 84)|<code>Required</code>, if relevant|
|:---|:---|
|Proposed Element Name|decimalLatitude|
|Example|5.89634|
|Definition|Latitude of the location where the sample was collected, entered in decimal degrees. Negative values for South latitudes.|
|Additional Instructions|Please supply no more than 6 decimal places (meter scale resolution) in the actual number (not just display format.) No letters are allowed.|

|Longitude (Coordinate system: WGS 84)|<code>Required</code>, if relevant|
|:---|:---|
|Proposed Element Name|decimalLongitude|
|Example|-103.785|
|Definition|Longitude of the location where the sample was collected, entered in decimal degrees. Negative values for ‘West’ longitudes.|
|Additional Instructions|Please supply no more than 6 decimal places (meter scale resolution) in the actual number (not just display format.) No letters are allowed.|

|Coordinate Uncertainty In Meters|code>Recommended</code>, Not in SESAR|
|:---|:---|
|Proposed Element Name|coordinateUncertaintyInMeters|
|Example|30 (reasonable lower limit of a GPS reading under good conditions if the actual precision was not recorded at the time)|
|Definition|The horizontal distance (in meters) from the given decimalLatitude and decimalLongitude describing the smallest circle containing the whole of the Location. Leave the value empty if the uncertainty is unknown, cannot be estimated, or is not applicable (because there are no coordinates). Zero is not a valid value for this term. In most cases, a value reflecting the precision and accuracy of the GPS instrument used to obtain coordinates is appropriate here.  Many GPS instruments will provide a precision along with coordinates that can be applied here.  |
|Additional Instructions||

|Navigation type|<code>Recommended</code>|
|:---|:---|
|Proposed Element Name|geolocationInstrument|
|Example|GPS; RTK GPS|
|Definition|Type of geolocation instrument used to obtain geographic coordinates.|
|Additional Instructions|[Please use controlled list](http://www.marine-geo.org/tools/search/vocab.php?use_is_displayed=T&vocab=vocab_nav_type).|

|Location description|<code>Recommended</code>|
|:---|:---|
|Proposed Element Name|locationDescription|
|Example|300 year old low-land tropical rainforest in Parque Natural San Lorenzo, Panama|
|Definition|Free text description of the location.|
|Additional Instructions|You can also include details here about the location type, e.g. whether it is an absolute or reference location, plot ID and description.|

|Country|<code>Recommended</code>|
|:---|:---|
|Proposed Element Name|country|
|Example|United States|
|Definition|Country where the sample was collected.|
|Additional Instructions|[Use controlled list](https://www.geosamples.org/help/vocabularies/country).|

|Elevation start|<code>Optional</code>|
|:---|:---|
|Proposed Element Name|minimumElevationInMeters|
|Example|678.5|
|Definition|Elevation at which a sample was collected. Minimum elevation value if elevation taken over a range.|
|Additional Instructions|Provide elevation in meters where possible.|

|Elevation end|<code>Optional</code>|
|:---|:---|
|Proposed Element Name|maximumElevationInMeters|
|Example|689.2|
|Definition|Maximum elevation at which a sample was collected, if elevation was taken over a range. |
|Additional Instructions|Provide elevation in meters where possible.|

|Elevation unit|<code>Optional</code>|
|:---|:---|
|Proposed Element Name||
|Example|meters|
|Definition|Unit in which elevation start and/or end are provided in. This will be removed when elevation field is changed to specify meters.  |
|Additional Instructions|Must be one of the following: meters, feet, miles, kilometers|

|Depth in Core (min)|<code>Required</code>, if relevant|
|:---|:---|
|Proposed Element Name|minimumDepthInMeters|
|Example|0.001|
|Definition|Minimum depth at which a sample was collected, below ground or under water.|
|Additional Instructions|Recommend using meters.|

|Depth in Core (max)|<code>Optional</code>|
|:---|:---|
|Proposed Element Name|maximumDepthInMeters|
|Example|0.003|
|Definition|Maximum depth at which a sample was collected, below ground or under water. |
|Additional Instructions|Recommend using meters|

|Depth scale|<code>Required</code>, if relevant|
|:---|:---|
|Proposed Element Name|NA, proposing that depth be required in meters|
|Example|meters|
|Definition|Unit in which the depth is provided|
|Additional Instructions|This field will be deleted when we change the depth field to be required in meters|

|Minimum Distance above Surface in Meters|<code>Optional</code>| 
|:---|:---|
|Proposed Element Name|minimumDistanceAboveSurfaceInMeters|
|Example|4.2|
|Definition|Minimum height above the ground surface, in meters.  If no range of values collected, provide height measurement here|
|Additional_instructions||

|Maximum Distance above Surface in Meters|<code>Optional</code>| 
|:---|:---|
|Proposed_element_name|maximumDistanceAboveSurfaceInMeters|
|Example|7.2|
|Definition|Maximum height above the ground surface, in meters.|
|Additional_instructions||

---

## Environmental Context

|Primary Physiographic feature|<code>Recommended</code>|
|:---|:---|
|Proposed Element Name|localEnvironmentalContext|
|Example|river [ENVO:00000022]; pond [ENVO:00000033]; wet meadow ecosystem [ENVO:01000449]; mountain [ENVO:00000081]|
|Definition|Entity or entities which are in your sample or specimen’s local vicinity and which you believe have significant causal influences on your sample or specimen. |
|Additional Instructions|Use terms that are present in the Environment Ontology (ENVO) and which are of smaller spatial grain than your entry for biome. We recommend using the Ontology Lookup Service (https://www.ebi.ac.uk/ols/ontologies/envo) to locate appropriate terms. Delimit multiple values using semi-colon. Example: Annotating a pooled sample taken from various vegetation layers in a forest consider: canopy [ENVO:00000047]; herb and fern layer [ENVO:01000337]; litter layer [ENVO:01000338]; understory [01000335]; shrub layer [ENVO:01000336]. If needed, request new terms on the ENVO tracker, [identified here](http://www.obofoundry.org/ontology/envo.html).|

|Biome|<code>Recommended</code>, Not in SESAR|
|:---|:---|
|Proposed Element Name|biome|
|Example|shrubland biome [ENVO:01000176]; tropical moist broadleaf forest biome [ENVO:01000228]; estuarine biome [ENVO:01000020]|
|Definition|Major environmental system your sample or specimen came from. The systems identified should have a coarse spatial grain, to provide the general environmental context of where the sampling was done (e.g. were you in the desert or a rainforest?).|
|Additional Instructions|We recommend using subclasses of [ENVO’s biome class](http://purl.obolibrary.org/obo/ENVO_00000428). If needed, request new terms on the ENVO tracker, [identified here](http://www.obofoundry.org/ontology/envo.html).|

---  

## Sample Access

|Release Date|<code>Required</code>|
|:---|:---|
|Proposed_element_name|releaseDate|
|Example|2018-03-15|
|Definition|Date when sample metadata should be publicly accessible and searchable. If null, defaults to date of registration in SESAR (recommended). |
|Additional_instructions|SESAR recommends that sample metadata become public within 2 years of sample registration.|

|Current Archive|<code>Optional</code>|
|:---|:---|
|Proposed_element_name|currentArchive|
|Example|Geosciences and Environmental Change Science Center, USGS Federal Center, Lakewood, CO|
|Definition|Name of institution, museum, or repository where the sample is currently stored.|
|Additional_instructions|Only applies to physical samples that are archived in a collection for some period of time.|

|Current Archive Contact|<code>Optional</code>|
|:---|:---|
|Proposed_element_name|currentArchiveContact|
|Example|scientist@lbl.gov|
|Definition|Address and/or email of the person who should be contacted for information about or access to the sample.|
|Additional_instructions|Email is not mandatory, but helps with communication about samples.|

