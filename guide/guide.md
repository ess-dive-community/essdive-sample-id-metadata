# ESS-DIVE Sample ID and Metadata Guide

Here you will find proposed guidelines for standardizing sample metadata to describe interdisciplinary samples within DOE's Environmental Systems Science community.

ESS-DIVE recommends obtaining International General Sample Numbers (IGSNs) for samples from the System for Earth Sample Registration (SESAR). Most of this proposed sample standard follows SESAR's metadata guidelines. However, we have proposed changes to metadata elements, specific requirements, and vocabularies based on ESS community needs. 

We seek any additional feedback, with the goal of making ESS sample information **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable (FAIR). 

---  
**Categories of Sample Metadata:**

- [Header Rows](#header-rows)
- [Sample IDs and Related Identifiers](#sample-ids-and-related-identifiers)
- [Sample Description](#sample-description)
- [Location](#location)
- [Sample Access](#sample-access)

---  

## Header Rows

|Object Type| <code> Mandatory </code>|
|:---|:---|
|Proposed Element Name|objectType|
|Examples|Core; Individual Sample|
|Definition|Broad characterization of the nature of a sample or specimen.|
|Additional Instructions|[Use controlled list.](https://www.geosamples.org/help/vocabularies#object) See [object type crosswalk](https://docs.google.com/spreadsheets/d/1kBETFbNoMfkgxbVhqiEJppCT2GaZYJUywucSKdblVJM/edit#gid=625226234) for revised terms proposed for ESS-DIVE, and provide feedback on additional terms or revisions needed.

|User Code|<code> Mandatory </code>|
|:---|:---|
|Proposed Element Name|userCode|
|Example|IEMEG|
|Definition|Three-letter code that will be used as a prefix for IGSNs in the submitted batch template.|
|Additional Instructions|User codes should be unique to an individual or large project managed by a team; avoid creating multiple user codes. If assigning IGSNs in the IGSN column, the user code must match the user code in the IGSNs. For example, if the user specifies IEMEG is the user code, any user-specified IGSNs must begin with IEMEG. If you do not specify the user code to be used, a default user code belonging to the registrant will be used.|

---  

## Sample IDs and Related Identifiers

|Sample Name|<code> Mandatory </code>|
|:---|:---|
|Proposed Element Name|sampleName|
|Example|001-ER18-FO|
|Definition|Collector's project-specific sample name, which must be unique for each sample that you are submitting.|
|Additional Instructions|This Sample Name is a place where you can develop a sample ID that has meaning to you and may help in your internal, project sample management.|

|Other name(s)|<code> Optional </code>
|:---|:---|
|Proposed Element Name|otherName|
|Example|001ER18FO; 001ER18-FO|
|Definition|Other sample name(s) that have been used in the past. |
|Additional Instructions|Use a semi-colon to delimit multiple names where needed.|

|IGSN|<code> Recommended </code>|
|:---|:---|
|Proposed Element Name|IGSN|
|Example|IEMEG0001|
|Definition|Globally unique and persistent identifier for the sample. Leave blank if you want SESAR to assign the IGSN, which is recommended. |
|Additional Instructions|For split samples/subsamples, you can assign your own 1-2 character extensions from the Parent IGSN, and submit your own IGSNs for registering these child samples.  This is not required, but is an option if desired. For assigning your own IGSNS, you must use upper-case alpha-numeric characters. |

|Parent IGSN|<code>Required</code>, if relevant|
|:---|:---|
|Proposed Element Name|parentIGSN|
|Example|IEMEG0002|
|Definition|The larger sample from which a child sample was derived. For example, a core section may be the parent of a series of subsamples or split samples. Parent and child samples are linked in the SESAR catalog. Sibling samples are inferred from parent-child relationships and are linked on the landing page for a sample.    |
|Additional Instructions|Leave blank if a parent IGSN does not exist. |

|Collection ID|<code>Optional</code>, Not in SESAR|
|:---|:---|
|Proposed Element Name|collectionID|
|Example|WSFA_June2019|
|Definition|A unique identifier for the set of information associated with a collection of samples; collections may be organized around a particular project, data set, field season, region, site, etc. A collection identifier can be used to link a set of samples together, and/or to enable efficient entry of metadata that is the same across all samples in a "sample collection." |
|Additional_instructions|Must be unique within the data package (project-assigned, and does not need to be globally unique). See link to diagram that demonstrates linking related collection, site, event, and sample IDs.  |

|Event ID|<code>Optional</code>, Not in SESAR|
|:---|:---|
|Proposed Element Name|eventID|
|Example|WSFA_20191023|
|Definition|A unique identifier for the set of information associated with an Event (something that occurs at a place and time). An event identifier can be used to link a set of samples collected on a specific date,  and/or to enable efficient entry of metadata that is the same across these samples.|
|Additional_instructions|Must be unique within the data package (project-assigned, and does not need to be globally unique). See link to diagram that demonstrates linking related collection, site, event, and sample IDs.  |

|Site ID|<code>Optional</code>, Not in SESAR|
|:---|:---|
|Proposed_element_name|siteID|
|Example|CoyoteRiver_D22|
|Definition|A unique identifier for the set of site location information. May be a global unique identifier or an identifier specific to the data set. For ESS-DIVE, a site identifier can be used to link a set of samples collected from a specific site,  and/or to enable efficient entry of metadata that is the same across these samples.|
|Additional_instructions|Must be unique within the data package (project-assigned, and does not need to be globally unique). See link to diagram that demonstrates linking related collection, site, event, and sample IDs.  |

---  

## Sample Description

|Material|
|:---|:---|
|Proposed_element_name|material|
|Optionality|Mandatory (SESAR)|
|Example|soil; sediment; surface water [ENVO:00002042]; groundwater [ENVO:01001004] |
|Definition|Material that the sample consists of. Mandatory.|
|Additional_instructions|Please use controlled list . ESS-DIVE requesting additional terms for organisms, organic material, and water samples, see: https://docs.google.com/spreadsheets/d/1fdI1x_nRUcGgcgWhwJZVNkNhVhTUPbHmB0inUEXcDUE/edit?ts=5eeb9683#gid=405062981 . |

|SESAR_element_name|Field name (informal classification)|
|:---|:---|
|Proposed_element_name|classification|
|Optionality|Optional|
|Example|leaf, root|
|Definition|Informal classification of sample. |
|Additional_instructions|free-text. Here you can add additional material classifications in the current SESAR IGSN controlled fields.  We will remove this field when object-type and material controlled terms are revised and expanded to accomodate ESS sample types.  |

|SESAR_element_name|Sample Description|
|:---|:---|
|Proposed_element_name|sampleDescription|
|Optionality|Recommended|
|Example|Day 223 core section from unheated control plot 1C of a deep soil warming experiment; Filter used for filtered surface water samples|
|Definition|Free text to describe features of a sample such as its components, texture, color, shape, treatments, plot ID from which the sample was taken, etc.|
|Additional_instructions|free-text|

|SESAR_element_name|Collection method description|
|:---|:---|
|Proposed_element_name|collectionMethodDescription|
|Optionality|Required|
|Example|Example 1) "Collect soil samples from top 10 cm using 2-3 cores from with meadow plot or under the bulk of tree/shrub canopies."  Example 2) Excised branch. Example 3) Pumped water at specific depths using tubing connected to CTD.|
|Definition|Free text description of the collection method for the sample. Include any important terms and details for potential users to understand how your sample was collected.|
|Additional_instructions|free-text. Collection methods may often be the same across a series/collection of samples; there are two options for providing collection method details at a higher level. Option 1:  Create a separate file with metadata to describe a sample collection, which contains a "collectionID", and any associated metadata fields (e.g. "collectionMethodDescription", "Purpose", "Chief Scientist", etc.).  Option 2: Create a methods file, with a series of methods descriptions that are each associated with a "methodID" and an associated "methodDescription." |

|SESAR_element_name|Purpose|
|:---|:---|
|Proposed_element_name|purpose|
|Optionality|Recommended|
|Example|Characterize the biogeochemistry, geochemistry and microbiology of soils associated with trees and shrubs. |
|Definition|The purpose for collecting the sample. |
|Additional_instructions|free-text. Purpose may often be the same across a series/collection of samples; To avoid entering the same information across numerous samples, you can create a separate file with metadata to describe a sample collection, which contains a "collectionID", and any associated metadata fields (e.g. "collectionMethodDescription", "Purpose", "Chief Scientist", etc.). |

|SESAR_element_name|Size|
|:---|:---|
|Proposed_element_name|size|
|Optionality|Optional|
|Example|4; 6.8|
|Definition|Size of the registered object, such as the surface area, length of a core, weight, or volume|
|Additional_instructions||

|SESAR_element_name|Size unit|
|:---|:---|
|Proposed_element_name|sizeUnit|
|Optionality|Optional|
|Example|square centimeter; kilogram|
|Definition|Unit for the numerical value provided for ‘size’.|
|Additional_instructions|Choose unit terms from the controlled list.  |

---  

## Location  

|SESAR_element_name|Latitude (Coordinate system: WGS 84)|
|:---|:---|
|Proposed_element_name|decimalLatitude|
|Optionality|Required, if relevant|
|Example|5.89634|
|Definition|Latitude of the location where the sample was collected, entered in decimal degrees. Negative values for South latitudes.|
|Additional_instructions|Please supply no more than 6 decimal places (meter scale resolution) in the actual number (not just display format.) No letters are allowed.|

|SESAR_element_name|Longitude (Coordinate system: WGS 84)|
|:---|:---|
|Proposed_element_name|decimalLongitude|
|Optionality|Required, if relevant|
|Example|-103.785|
|Definition|Longitude of the location where the sample was collected, entered in decimal degrees. Negative values for ‘West’ longitudes.|
|Additional_instructions|Please supply no more than 6 decimal places (meter scale resolution) in the actual number (not just display format.) No letters are allowed.|

|SESAR_element_name|Elevation start|
|:---|:---|
|Proposed_element_name|minimumElevationInMeters|
|Optionality|Optional|
|Example|678.5|
|Definition|Elevation at which a sample was collected. Minimum elevation value if elevation taken over a range.|
|Additional_instructions||

|SESAR_element_name|Elevation end|
|:---|:---|
|Proposed_element_name|maximumElevationInMeters|
|Optionality|Optional|
|Example|689.2|
|Definition|Maximum elevation at which a sample was collected, if elevation was taken over a range. |
|Additional_instructions||

|SESAR_element_name|Elevation unit|
|:---|:---|
|Proposed_element_name||
|Optionality|Optional|
|Example|meters|
|Definition|Unit in which elevation start and/or end are provided in. This will be removed when elevation field is changed to specify meters.  |
|Additional_instructions|Must be one of the following: meters, feet, miles, kilometers|

|SESAR_element_name|Navigation type|
|:---|:---|
|Proposed_element_name|geolocationInstrument|
|Optionality|Recommended|
|Example|GPS; RTK GPS|
|Definition|Type of geolocation instrument used to obtain geographic coordinates.|
|Additional_instructions|Please use controlled list|

|SESAR_element_name|Primary Physiographic feature|
|:---|:---|
|Proposed_element_name|localEnvironmentalContext|
|Optionality|Recommended|
|Example|river [ENVO:00000022]; pond [ENVO:00000033]; wet meadow ecosystem [ENVO:01000449]; mountain [ENVO:00000081]|
|Definition|Entity or entities which are in your sample or specimen’s local vicinity and which you believe have significant causal influences on your sample or specimen. |
|Additional_instructions|Please use terms that are present in ENVO and which are of smaller spatial grain than your entry for env_broad_scale. Use ENVO terms, using the Ontology Lookup Service (https://www.ebi.ac.uk/ols/ontologies/envo). Delimit multiple values using semi-colon. Example: Annotating a pooled sample taken from various vegetation layers in a forest consider: canopy [ENVO:00000047]; herb and fern layer [ENVO:01000337]; litter layer [ENVO:01000338]; understory [01000335]; shrub layer [ENVO:01000336]. If needed, request new terms on the ENVO tracker, identified here: http://www.obofoundry.org/ontology/envo.html|

|SESAR_element_name|Location description|
|:---|:---|
|Proposed_element_name|locationDescription|
|Optionality|Recommended|
|Example|300 year old low-land tropical rainforest in Parque Natural San Lorenzo, Panama|
|Definition|Free text description of the location. You can also include details here also about the location type, e.g. whether it is an absolute or reference location, plot ID and description.|
|Additional_instructions||

|SESAR_element_name|Country|
|:---|:---|
|Proposed_element_name|country|
|Optionality|Required|
|Example|United States|
|Definition|Country where the sample was collected|
|Additional_instructions|Please use controlled list. |

|SESAR_element_name|Depth in Core (min)|
|:---|:---|
|Proposed_element_name|minimumDepthInMeters|
|Optionality|Required, if relevant|
|Example|0.001|
|Definition|Minimum depth at which a sample was collected, below ground or under water. |
|Additional_instructions|Recommend using meters|

|SESAR_element_name|Depth in Core (max)|
|:---|:---|
|Proposed_element_name|maximumDepthInMeters|
|Optionality|Required, if relevant|
|Example|0.003|
|Definition|Maximum depth at which a sample was collected, below ground or under water. |
|Additional_instructions|Recommend using meters|

|SESAR_element_name|Depth scale|
|:---|:---|
|Proposed_element_name||
|Optionality|Required, if relevant|
|Example|meters|
|Definition|Unit in which the depth is provided|
|Additional_instructions||

|SESAR_element_name|Field program/Cruise|
|:---|:---|
|Proposed_element_name|projectName|
|Optionality|Required at package level, but want associated with samples when searched.|
|Example|Next Generation Ecosystem Experiments (NGEE) Tropics; LBNL Watershed Function SFA |
|Definition|Enter the name of the DOE project to associate with this/these sample(s).|
|Additional_instructions|If multiple projects were involved, enter the project that had the largest contribution to this data package first, and separate entries with a semi-colon. Project Name may often be the same across a series/collection of samples; To avoid entering the same information across numerous samples, you can create a separate file with metadata to describe a sample collection, which contains a "collectionID", and any associated metadata fields (e.g. "Project Name", "collectionMethodDescription", "Purpose", "Chief Scientist", etc.).  |

|SESAR_element_name|Collector/Chief Scientist|
|:---|:---|
|Proposed_element_name|collector|
|Optionality|Required|
|Example|John Smith|
|Definition|Name of the person(s) who collected the sample. You can enter multiple collectors/sampling team for large sampling efforts. If the collector(s) of the sample(s) is/are not known, enter name of the person responsible for the sample. |
|Additional_instructions|Separate multiple entries with a semi-colon|

|SESAR_element_name|Collection date|
|:---|:---|
|Proposed_element_name|collectionDate|
|Optionality|Required|
|Example|3/31/15|
|Definition|Date when the sample was collected. YYYY-MM-DD|
|Additional_instructions|All dates and times must be reported in Coordinated Universal Time (UTC) and follow the ISO 8601 standard (RFC 3339). Temporal data using different standards can be provided as a separate variable (column) in addition to UTC format.|

|SESAR_element_name|Collection time|
|:---|:---|
|Proposed_element_name|collectionTime|
|Optionality|Optional|
|Example|12:05:03Z|
|Definition|Time when the sample was collected. HH:MM:SSZ|
|Additional_instructions|All dates and times must be reported in Coordinated Universal Time (UTC) and follow the ISO 8601 standard (RFC 3339). Temporal data using different standards can be provided as a separate variable (column) in addition to UTC format.|

|SESAR_element_name|Current Archive|
|:---|:---|
|Proposed_element_name|currentArchive|
|Optionality|Optional|
|Example|Geosciences and Environmental Change Science Center, USGS Federal Center, Lakewood, CO|
|Definition|Only applies to physical samples that are archived in a collection for some period of time. Name of institution, museum, or repository where the sample is currently stored.|
|Additional_instructions||

|SESAR_element_name|Current Archive Contact|
|:---|:---|
|Proposed_element_name|currentArchiveContact|
|Optionality|Optional|
|Example|scientist@lbl.gov|
|Definition|Address and/or email of the person who should be contacted for information about or access to the sample.|
|Additional_instructions|Email is not mandatory, but helps for communication about samples.|

|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|biome|
|Optionality|Recommended|
|Example|shrubland biome [ENVO:01000176]; tropical moist broadleaf forest biome [ENVO:01000228]; estuarine biome [ENVO:01000020]|
|Definition|Report which major environmental system your sample or specimen came from. The systems identified should have a coarse spatial grain, to provide the general environmental context of where the sampling was done (e.g. were you in the desert or a rainforest?). |
|Additional_instructions|We recommend using subclasses of ENVO’s biome class: http://purl.obolibrary.org/obo/ENVO_00000428. Format (one term): termLabel [termID]. Multiple terms can be separated by a semi-colon. If needed, request new terms on the ENVO tracker, identified here: http://www.obofoundry.org/ontology/envo.html|


|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|coordinateUncertaintyInMeters|
|Optionality|Recommended|
|Example|30 (reasonable lower limit of a GPS reading under good conditions if the actual precision was not recorded at the time)|
|Definition|The horizontal distance (in meters) from the given decimalLatitude and decimalLongitude describing the smallest circle containing the whole of the Location. Leave the value empty if the uncertainty is unknown, cannot be estimated, or is not applicable (because there are no coordinates). Zero is not a valid value for this term. In most cases, a value reflecting the precision and accuracy of the GPS instrument used to obtain coordinates is appropriate here.  Many GPS instruments will provide a precision along with coordinates that can be applied here.  |
|Additional_instructions||

|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|minimumDistanceAboveSurfaceInMeters|
|Optionality|Optional|
|Example|4.2|
|Definition|Minimum height above the ground surface, in meters.  If no range of values collected, provide height measurement here|
|Additional_instructions||

|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|maximumDistanceAboveSurfaceInMeters|
|Optionality|Optional|
|Example|7.2|
|Definition|Maximum height above the ground surface, in meters.|
|Additional_instructions||

|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|sampleProcessing|
|Optionality|Recommended, if relevant|
|Example|filter water; store samples in ethanol|
|Definition|Any processing applied to the sample during or after retrieving the sample from environment. Can provide a list of preparations and preservation methods for the sample. Separate multiple processes with a semi-colon.      |
|Additional_instructions||

|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|filterSize|
|Optionality|Required if object type is filter, or for a filtered sample (e.g. water sample)|
|Example|0-0.22 micrometer|
|Definition|Filtering pore size used in sample preparation (filter size value range). Filter size value range (float-float unit).|
|Additional_instructions||

|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|scientificName|
|Optionality|Required, if relevant|
|Example|Vochysia ferruginea; Miconia borealis; Terminalia amazonia|
|Definition|The full scientific name, with authorship and date information if known. When forming part of an Identification, this should be the name in lowest level taxonomic rank that can be determined.|
|Additional_instructions||

|SESAR_element_name|Not represented|
|:---|:---|
|Proposed_element_name|comments|
|Optionality|Optional|
|Example||
|Definition|Comments or notes about the sample. |
|Additional_instructions|Free text. You can include weather descriptions here, if relevant |

---  

## Sample Access

|Release Date|<code>Required</code>|
|:---|:---|
|Proposed_element_name|releaseDate|
|Example|2018-03-15|
|Definition|Date when sample metadata should be publicly accessible and searchable. If null, defaults to date of registration in SESAR (recommended). |
|Additional_instructions|SESAR recommends that sample metadata become public within 2 years of sample registration.|
