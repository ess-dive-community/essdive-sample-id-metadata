# ESS-DIVE Sample ID and Metadata Guide

Here you will find proposed guidelines for standardizing sample metadata to describe interdisciplinary samples within DOE's Environmental Systems Science community.

Most of the sample metadata follows [SESAR's metadata guidelines](http://doi.org/10.5281/zenodo.3874923). However, we modified some metadata elements, specific requirements, and vocabularies based on ESS community needs. This includes additional fields, which mostly come from biodiversity standards [Darwin Core](https://dwc.tdwg.org/), or genomic standards [Minimum Information about any Sequence (MIxS)](https://gensc.org/mixs/). 

We seek any additional feedback, with the goal of making ESS sample information **F**indable, **A**ccessible, **I**nteroperable, and **R**eusable (FAIR). 

---  
## Sample Metadata Content - Link to More Details
*Required fields are marked with an asterisk, and indicated in detailed tables below.

**[Header Rows](#header-rows)**:      
[Object Type*](#object-type) |
[User Code*](#user-code)

**[Sample IDs and Related Identifiers](#sample-ids-and-related-identifiers)**:     
[Sample Name*](#sample-name) |
[Other names](#other-names) |
[IGSN](#igsn) |
[Parent IGSN](#parent-igsn) |
[Collection ID](#collection-id) |
[Event ID](#event-id) |
[Location ID](#location-id)

**[Sample Description](#sample-description)**:     
[Material*](#material) |
[Field name informal classification](#field-name-informal-classification) |
[Sample Description](#sample-description) |
[Purpose](#purpose) |
[Size](#size) |
[Size unit](#size-unit) |
[Filter Size](#filter-size) |
[Filter Size Unit](#filter-size-unit) |
[Scientific Name](#scientific-name) |
[Comment](#comment)

**[Sample Collection Details](#sample-collection-details)**:     
[Collector / Chief Scientist*](#collector-chief-scientist) |
[Collection Date*](#collection-date) | 
[Collection Time](#collection-time) | 
[Collection Method](#collection-method) |
[Collection Method Description*](#collection-method-description) | 
[Sample Processing](#sample-processing) | 
[Field Program / Cruise*](#field-program-cruise)

**[Location](#location)**:     
[Latitude*](#latitude) | 
[Longitude*](#longitude) | 
[Navigation Type](#navigation-type) | 
[Location Description](#location-description) | 
[Country](#country) | 
[Elevation start](#elevation-start) | 
[Elevation end](#elevation-end) | 
[Elevation unit](#elevation-unit) | 
[Depth in Core (min)](#depth-in-core-min) | 
[Depth in Core (max)](#depth-in-core-max) | 
[Depth scale](#depth-scale) | 
[Minimum Distance above Surface in Meters](#minimum-distance-above-surface-in-meters) | 
[Maximum Distance above Surface in Meters](#maximum-distance-above-surface-in-meters) | 

**[Environmental Context](#environmental-context)**:      
[Primary Physiographic feature*](#primary-physiographic-feature) | 
[Biome](#biome)

**[Sample Access](#sample-access)**:     
[Release Date](#release-date) | 
[Current Archive](#current-archive) | 
[Current Archive Contact](#current-archive-contact) |
[Related URL](#related-url) |
[Related URL Type](#related-url-type) |
[Related URL Description](#related-url-description)

---  
## Header Rows

### Object Type
|Metadata Element|<div align="center">Object Type<div>| 
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required |
|**Definition**           |Broad characterization of the nature of a sample or specimen.|
|**Format**               |[SESAR Controlled List](https://www.geosamples.org/help/vocabularies#object). See [object type list](terms/objectType.md) for revised terms proposed for ESS-DIVE|
|**Additional Instructions**|Provide feedback on additional terms or revisions needed.
|**Examples**             |Core; Individual Sample; Organism|

### User Code 
|Metadata Element|<div align="center">User Code</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required |
|**Definition**           |Globally unique IGSN code that will be used as a prefix <br>for IGSNs in the submitted batch template.|
|**Format**               |Five-letter code                                     |
|**Additional Instructions**|User codes should be unique to an individual or large project managed by a team;<br> avoid creating multiple user codes. If assigning IGSNs in the IGSN column, <br>the user code must match the user code in the IGSNs. For example, if the user <br>specifies IEMEG is the user code, any user-specified IGSNs must begin with IEMEG.<br> If you do not specify the user code to be used, a default user code belonging<br> to the registrant will be used.|
|**Examples**             |IEMEG, IEJDE                                        |

---  
## Sample IDs and Related Identifiers

### Sample Name
|Metadata Element|<div align="center">Sample Name</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required |
|**Definition**           |Collector's project-specific sample name, which must be unique for each sample that<br> you are submitting.|
|**Format**               |free text, unique                                    |
|**Additional Instructions**|You can develop a sample ID that has meaning to you and may help in your internal, <br>project sample management.|
|**Examples**             |001-ER18-FO                                          |

### Other names 
|Metadata Element|<div align="center">Other name(s)</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional |
|**Definition**           |Other sample name(s) that have been used in the past.<img width=220/>|
|**Format**               |free text                                            |
|**Additional Instructions**|Use a semi-colon to delimit multiple names where needed.|
|**Examples**             |001ER18FO; 001ER18-FO                                |

### IGSN
|Metadata Element|<div align="center">IGSN</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Recommended |
|**Definition**           |Globally unique and persistent identifier for the sample. Leave blank if you want <br>SESAR to assign the IGSN, which is recommended.|
|**Format**               |semi-opaque, alphanumeric characters (9 recommended) |
|**Additional Instructions**|For split samples/subsamples, you can assign your own 1-2 character extensions from <br> the Parent IGSN, and submit your own IGSNs for registering these child samples.<br>  This is not required, but is an option if desired. For assigning your own<br> IGSNS, you must use upper-case alpha-numeric characters.|
|**Examples**             |IEWER7214, IEMEG0215, 10.58052/IEAMN007P                                 |

### Parent IGSN 
|Metadata Element|<div align="center">Parent IGSN</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If relevant, <code>Required |
|**Definition**           |The larger sample from which a child sample was derived. For example, a core section<br> may be the parent of a series of subsamples or split samples. Parent<br> and child samples are linked in the SESAR catalog. Sibling samples are inferred<br> from parent-child relationships and are linked on the landing page for a<br> sample.|
|**Format**               |semi-opaque, alphanumeric characters (9 recommended) | 
|**Additional Instructions**|Leave blank if a parent IGSN does not exist.|
|**Examples**              |IEMEG0002, 10.58052/IEMEG0004                                    |

### Collection ID 
_Not a SESAR Field_
|Metadata Element|<div align="center">Collection ID</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional |
|**Definition**           |A unique identifier for the set of information associated with a collection of<br> samples; collections may be organized around a particular project, data set,<br> field season, region, site, etc. |
|**Format**               |free text, unique                                    |
|**Additional Instructions**|Must be unique within the data package (project-assigned, and does not need<br> to be globally unique). See link to diagram that demonstrates linking related<br> collection, site, event, and sample IDs. A collection identifier can be<br> used to link a set of samples together, and/or to enable efficient entry of<br> metadata that is the same across all samples in a "sample collection."|
|**Examples**             |WSFA_June2019                                        |

### Event ID 
_Not a SESAR Field_
|Metadata Element|<div align="center">Event ID</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional |
|**Definition**           |A unique identifier for the set of information associated with an Event <br>(something that occurs at a place and time).|
|**Format**               |free text, unique                                    |
|**Additional Instructions**|Must be unique within the data package (project-assigned, and does not need <br> to be globally unique). See link to diagram that demonstrates linking related<br> collection, site, event, and sample IDs. An event identifier can be used to<br> link a set of samples collected on a specific date,  and/or to enable efficient<br> entry of metadata that is the same across these samples.|
|**Examples**             |WSFA_20191023                                        |

### Location ID
_Not a SESAR Field_
|Metadata Element|<div align="center">Location ID</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional |
|**Definition**           |A unique identifier for the set of location information. May be a global<br> unique identifier or an identifier specific to the data set.|
|**Format**               |free text, unique                                    |
|**Additional Instructions**|Must be unique within the data package (project-assigned, and does not need to<br> be globally unique). See link to diagram that demonstrates linking related<br> collection, site, event, and sample IDs. A site identifier can be used to link<br> a set of samples collected from a specific site,  and/or to enable<br> efficient entry of metadata that is the same across these samples. |
|**Examples**             |CoyoteRiver_D22                                      |

---  

## Sample Description

### Material 
|Metadata Element|<div align="center">Material</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required |
|**Definition**           |Material that the sample consists of.                |
|**Format**               |[SESAR controlled list.](https://app.geosamples.org/reference/materials.php)See ESS-DIVE's proposed [material terms](terms/material.md) from Environment<br> Ontology (ENVO)|
|**Additional Instructions**|Use a semi-colon to delimit multiple materials where needed. Please provide feedback<br> on any other terms needed.|
|**Examples**             |Soil; Sediment; Gas; Liquid>aqueous |


### Field name informal classification 
|Metadata Element|<div align="center">Field name (informal classification)</div>
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional |
|**Definition**           |Informal classification of sample                    |
|**Format**               |free text                                            |
|**Additional Instructions**|Here you can add additional material classifications that are not in the current SESAR<br> IGSN controlled fields. |
|**Examples**             |leaf, root, surface water, groundwater               |

### Sample Description 
|Metadata Element|<div align="center">Sample Description</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Recommended |
|**Definition**           |Description of sample features, such as its components, texture, color, shape,<br> treatments, plot ID from which the sample was taken, etc.|
|**Format**               |free-text                                            |
|**Additional Instructions**|                                                   |
|**Examples**             |Example 1) Day 223 core section from unheated control plot 1C of a deep soil warming<br> experiment; Example 2) Filter used for filtered surface water samples|

### Purpose                           
|Metadata Element|<div align="center">Purpose</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Recommended |
|**Definition**           |The scientific purpose for collecting the sample.    |
|**Format**               |free text                                            |
|**Additional Instructions**|Purpose may often be the same across a series/collection of samples;<br> To avoid entering the same information across numerous samples, you can create<br> a separate file with metadata to describe a sample collection, which contains<br> a "collectionID", and any associated metadata fields (e.g.<br> "collectionMethodDescription", "Purpose", "Chief Scientist", etc.).|
|**Examples**            |Characterize the biogeochemistry, geochemistry and microbiology of soils<br> associated with trees and shrubs.                     |

### Size
|Metadata Element|<div align="center">Size</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional |
|**Definition**           |Size of the registered object, such as the surface area, length of a core, weight,<br> or volume|
|**Format**               |Number                                               |
|**Additional Instructions**| Must be associated with Size unit. 
|**Examples**             |4; 6.8                                               |

### Size unit
|Metadata Element|<div align="center">Size unit</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If Size provided, <code>Required |
|**Definition**           |Unit for the numerical value provided for ‘size’.    |
|**Format**               |[Controlled List](terms/units.md)                    |
|**Additional Instructions**|Use any additional unit terms from [Units Ontology](http://www.ontobee.org/ontology/UO), and provide feedback.<img width=50/>|
|**Examples**             |square centimeter; kilogram                          |

### Filter Size
_Not a SESAR Field_
|Metadata Element|<div align="center">Filter Size</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | only if object type is "filtrate" or "material captured in filter", <code>Required |
|**Definition**           |Filtering pore size used in sample preparation (filter size value range). Filter size<br> value range.                                 |
|**Format**               |Number range (float-float)                           |
|**Additional Instructions**|                                                   |
|**Examples**             |0-0.22                                               |

### Filter Size Unit
_Not a SESAR Field_
|Metadata Element|<div align="center">Filter Size unit</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | only if object type is "filtrate" or "material captured in filter", <code>Required |
|**Definition**           |Filtering pore size unit.                            |
|**Format**               |unit (float-float unit)                              |
|**Additional Instructions**|                                                   |
|**Examples**             |micrometer                                           |

### Scientific Name
_Not a SESAR Field_
|Metadata Element|<div align="center">scientificName</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | only if object type is "Organism", <code>Required |
|**Definition**           |The full scientific name, with authorship and date information if known. When<br> forming part of an Identification, this should be the name in lowest level taxonomic<br> rank that can be determined.|
|**Format**               |                                                     |
|**Additional Instructions**|                                                   |
|**Examples**             |Vochysia ferruginea; Miconia borealis; Terminalia amazonia|

### Comment
|Metadata Element|<div align="center">Comment</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Comments or notes about the sample. <img width=250/> |
|**Format**               |free text                                            |
|**Additional Instructions** |You can include weather descriptions here, if relevant.|
|**Examples**             |                                                     |
---

## Sample Collection Details

### Collector Chief Scientist
|Metadata Element|<div align="center">Collector/Chief Scientist</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required|
|**Definition**           |Name of the person(s) who collected the sample.      |
|**Format**               |                                                     |
|**Additional Instructions**|You can enter multiple collectors/sampling team for large sampling efforts, separated<br> with a semi-colon. If the collector(s) of the sample(s) is/are not known,<br> enter name of the person responsible for the sample.|
|**Examples**             |John Smith; Jane Johnson|

### Collection Date
|Metadata Element|<div align="center">Collection date</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required|
|**Definition**           |Date when the sample was collected.                  |
|**Format**               |YYYY-MM-DD                                           |
|**Additional Instructions**|All dates and times must be reported in Coordinated Universal Time (UTC) and follow<br> the ISO 8601 standard (RFC 3339). Temporal data using different standards can be<br> provided as a separate variable (column) in addition to UTC format.|
|**Examples**             |2019-08-14                                           |

### Collection Time
|Metadata Element|<div align="center">Collection time</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Time when the sample was collected.                  |
|**Format**               |HH:MM:SSZ                                            |
|**Additional Instructions**|All dates and times must be reported in Coordinated Universal Time (UTC) and follow<br> the ISO 8601 standard (RFC 3339). Temporal data using different standards can be<br> provided as a separate variable (column) in addition to UTC format.|
|**Examples**             |12:05:03Z                                            |

### Collection Method
|Metadata Element|<div align="center">Collection method</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Method by which a sample was collected.                  |
|**Format**               |[SESAR controlled list.](http://www.geosamples.org/help/vocabularies#collection)                                            |
|**Additional Instructions**|Suggested to use SESAR's controllect list, if none applicable free text.|
|**Examples**             |Dredging; Manual                                            |

### Collection Method Description
|Metadata Element|<div align="center">Collection method description</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required|
|**Definition**           |Description of the collection method for the sample. Include any important terms <br>and details for potential users to understand how your sample was collected.|
|**Format**               |                                                     |
|**Additional Instructions**|Collection methods may often be the same across a series/collection of samples;<br> there are two options for providing collection method details at a higher level.<br> Option 1:  Create a separate file with metadata to describe a sample<br> collection, which contains a "collectionID", and any associated metadata fields<br> (e.g. "collectionMethodDescription", "Purpose", "Chief Scientist", etc.).<br>  Option 2: Create a methods file, with a series of methods descriptions<br> that are each associated with a "methodID" and an associated "methodDescription." |
|**Examples**             |Example 1) Collect soil samples from top 10 cm using 2-3 cores from with meadow<br> plot or under the bulk of tree/shrub canopies.  Example 2) Excised branch.<br> Example 3) Pumped water at specific depths using tubing connected to CTD.|

### Sample Processing
_Not a SESAR Field_
|Metadata Element|<div align="center">Sample processing</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | if relevant, <code>Recommended|
|**Definition**           |Any processing applied to the sample during or after retrieving the sample from the<br> environment. Can provide a list of preparations and preservation<br> methods for the sample.|
|**Format**               |                                                     |
|**Additional Instructions**|Sample processing may often be the same across a series/collection of samples.<br> To avoid entering the same information across numerous samples, you can create<br> a separate file with metadata to describe a sample collection, which contains<br> a "collectionID", and any associated metadata fields (e.g.<br> "sampleProcessing", "collectionMethodDescription", "Purpose", "Chief Scientist",<br> etc.). Separate multiple sample processing methods<br> with a semi-colon.|
|**Examples**             |filter water; store samples in ethanol|

### Field Program Cruise
|Metadata Element|<div align="center">Field program/cruise </div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required|
|**Definition**           |Enter the name of the DOE project to associate with this/these sample(s).|
|**Format**               |free text                                            |
|**Additional Instructions**|Required at dataset level, but want to associate with samples for data search<br> and integration. Project details may often be the same across a series/collection<br> of samples; To avoid entering the same information across numerous samples,<br> you can create a separate file with metadata to describe a project or<br> sample collection, which contains a "collectionID" or "Field Program/Cruise",<br> and any associated metadata fields (e.g. "Collection Method Description",<br> "Purpose", "Chief Scientist"...|
|**Examples**             |Next Generation Ecosystem Experiments (NGEE) Tropics; LBNL Watershed Function<br> SFA |

---  

## Location  

### Latitude
|Metadata Element|<div align="center">Latitude</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | if relevant, <code>Required|
|**Definition**           |Latitude of the location where the sample was collected, entered in decimal<br> degrees. Negative values for South latitudes.|
|**Format**               |Decimal degrees, coordinate system: WGS 84           |
|**Additional Instructions**|Please supply no more than 6 decimal places (meter scale resolution) in the actual<br> number (not just display format.) No letters are allowed.|
|**Examples**             |5.89634                                              |

### Longitude
|Metadata Element|<div align="center">Longitude</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | if relevant, <code>Required|
|**Definition**           |Longitude of the location where the sample was collected. Negative values <br> for ‘West’ longitudes.|
|**Format**               |Decimal degrees, coordinate system: WGS 84           |
|**Additional Instructions**|Please supply no more than 6 decimal places (meter scale resolution) in the actual<br> number (not just display format.) No letters are allowed.|
|**Examples**             |-103.785                                             |

### Navigation Type
|Metadata Element|<div align="center">Navigation type</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Recommended|
|**Definition**           |Type of geolocation instrument used to obtain geographic coordinates. <img width=20/>|
|**Format**               |[Controlled list](http://www.marine-geo.org/tools/search/vocab.php?use_is_displayed=T&vocab=vocab_nav_type).|
|**Additional Instructions**|Provide feedback on additional terms needed.|
|**Examples**             |GPS; RTK GPS|

### Location Description 
|Metadata Element|<div align="center">Location description</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Recommended|
|**Definition**           |Free text description of the location.|
|**Format**               |
|**Additional Instructions**|You can also include details here about the location type, e.g. whether it is an<br> absolute or reference location, plot ID and description.|
|**Examples**             |300 year old low-land tropical rainforest in Parque Natural San Lorenzo, Panama|

### Country
|Metadata Element|<div align="center">Country</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Required|
|**Definition**           |Country where the sample was collected. <img width=200/>|
|**Format**               |[SESAR controlled list](https://www.geosamples.org/help/vocabularies/country). <img width=150/>        |
|**Additional Instructions**|Use SESAR list, but may change controlled list to [GAZ ontology](http://purl.obolibrary.org/obo/gaz).                             |
|**Examples**             |United States                                        |

### Elevation start
|Metadata Element|<div align="center">Elevation start</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Elevation at which a sample was collected. Minimum elevation value, if elevation<br> taken over a range.|
|**Format**               |Number                                               |
|**Additional Instructions**|Provide elevation in meters where possible.|
|**Examples**             |678.5|

### Elevation end
|Metadata Element|<div align="center">Elevation end</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Maximum elevation at which a sample was collected, if elevation was taken over a<br> range. |
|**Format**               |Number                                               |
|**Additional Instructions**|Leave blank if elevation is a single value and not range. Provide elevation in<br> meters where possible.|
|**Examples**             |689.2                                                |

### Elevation unit
|Metadata Element|<div align="center">Elevation unit</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If relevant, <code>Required|
|**Definition**           |Unit that elevation start and/or end are provided in.   
|**Format**               |Recommend meters. <img width=200/>                   |
|**Additional Instructions**|This will be removed when elevation field is changed to specify meters. |
|**Examples**             |meters|

### Depth in Core min
|Metadata Element|<div align="center">Depth in Core (min)</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If relevant, <code>Required|
|**Definition**           |Depth, or minimum depth (if taken over a range) at which a sample was collected, <br>below ground or under water.                  |
|**Format**               |Number                                               |
|**Additional Instructions**|Recommend using meters.                            |
|**Examples**             |0.001                                                |

### Depth in Core max
|Metadata Element|<div align="center">Depth in Core (max)</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If relevant, <code>Required|
|**Format**               |Number                                               |
|**Definition**           |Maximum depth at which a sample was collected, below ground or under water. <img width=20/> |
|**Additional Instructions**|Recommend using meters.                            |
|**Examples**             |0.003|

### Depth scale
|Metadata Element|<div align="center">Depth scale</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If relevant, <code>Required|
|**Format**               |Recommend meters. <img width=150/>                   |
|**Definition**           |Unit in which the depth is provided, should be meters.|
|**Additional Instructions**|This field will be deleted when we change the depth field to be required in meters.|
|**Examples**             |meters|

### Minimum Distance above Surface in Meters
_Not a SESAR Field_
|Metadata Element|<div align="center">Minimum distance above surface in meters</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If relevant, <code>Required|
|**Definition**           |Minimum height above the ground surface, in meters.  If no range of values collected,<br> provide height measurement here.|
|**Format**               |Number                                               |
|**Additional Instructions**|                                                   |
|**Examples**             |4.2                                                  |

### Maximum Distance above Surface in Meters
_Not a SESAR Field_
|Metadata Element|<div align="center">Maximum distance above surface in meters</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | If relevant, <code>Required|
|**Definition**           |Maximum height above the ground surface, in meters.<img width=200/>|
|**Format**               |Number                                               |
|**Additional Instructions**|                                                   |
|**Examples**             |7.2                                                  |

---

## Environmental Context

### Primary physiographic feature
|Metadata Elementt|<div align="center">Primary physiographic feature</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Recommended|
|**Definition**           |Entity or entities which are in your sample or specimen’s local vicinity and<br> which you believe have significant causal influences on your sample or<br> specimen. |
|**Format**               |[Terms from Environment Ontology (ENVO)](https://www.ebi.ac.uk/ols/ontologies/envo). Provide the appropriate term and<br> ENVO identifier - see examples below.|
|**Additional Instructions**|Choose environmental context that is a smaller spatial grain than your entry <br> for biome. Delimit multiple values using semi-colon. If needed, request new<br> terms on the ENVO tracker, [identified here](http://www.obofoundry.org/ontology/envo.html).|
|**Examples**             |river [ENVO:00000022]; pond [ENVO:00000033]; wet meadow ecosystem<br> [ENVO:01000449]; mountain [ENVO:00000081] <br>_For annotating a pooled sample taken from various<br> vegetation layers in a forest, consider:_ canopy [ENVO:00000047]; herb and<br> fern layer [ENVO:01000337]; litter layer [ENVO:01000338];<br> understory [01000335]; shrub layer [ENVO:01000336].|

### Biome
_Not a SESAR Field_
|Metadata Element|<div align="center">Biome</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Recommended|
|**Definition**           |Major environmental system your sample or specimen came from. The systems<br> identified should have a coarse spatial grain, to provide the general environmental<br> context of where the sampling was done (e.g. were you in the desert or a<br> rainforest?).|
|**Format**               |[Terms from Environment Ontology (ENVO)](https://www.ebi.ac.uk/ols/ontologies/envo). Provide the appropriate term and ENVO<br> identifier - see examples below.|
|**Additional Instructions**|We recommend using subclasses of [ENVO’s biome class](http://purl.obolibrary.org/obo/ENVO_00000428). Use a semi-colon to delimit multiple biomes where needed. If needed, request new <br>terms on the ENVO tracker, [identified here](http://www.obofoundry.org/ontology/envo.html).|
|**Examples**             |shrubland biome [ENVO:01000176]; tropical moist broadleaf forest biome<br> [ENVO:01000228]; estuarine biome [ENVO:01000020]|

---  

## Sample Access

### Release Date  
|Metadata Element|<div align="center">Release Date</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Date when sample metadata should be publicly accessible and searchable. If null<br>, defaults to date of registration in SESAR (recommended). |
|**Format**               |YYYY-MM-DD                                           |
|**Additional Instructions**|SESAR recommends that sample metadata become public within 2 years of sample <br>registration.|
|**Examples**             |2018-03-15                                           |                    

### Current Archive 
|Metadata Element|<div align="center">Current archive</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Name of institution, museum, or repository where the sample is currently stored.|
|**Format**               |                                                     |
|**Additional Instructions**|Only applies to physical samples that are archived in a collection for some period<br> of time.|
|**Examples**             |Geosciences and Environmental Change Science Center, USGS Federal Center, Lakewood,<br> CO|

### Current Archive Contact
|Metadata Element|<div align="center">Current archive contact</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Address and/or email of the person who should be contacted for information about<br> or access to the sample.|
|**Format**               |free text                                            |
|**Additional Instructions**|Email is not mandatory, but helps with communication about samples.|
|**Examples**             |scientist@lbl.gov                                    |

### Related URL
|Metadata Element|<div align="center">Related URL</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Related URL associated with the samples.|
|**Format**               |Must be a valid URL (e.g., http://www.geosamples.org).|
|**Additional Instructions**|Email is not mandatory, but helps with communication about samples.|
|**Examples**             |https://data.ess-dive.lbl.gov/datasets/doi:10.15485/1830417|

### Related URL Type
|Metadata Element|<div align="center">Related URL Type</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Related URL type. Either DOI or Regular URL.|
|**Format**               |Must be either 'DOI' or 'Regular URL'.|
|**Additional Instructions**|         |
|**Examples**             |DOI|

### Related URL Description
|Metadata Element|<div align="center">Related URL Description</div>|
|:------------------------|:----------------------------------------------------|
|**Requirement Level** | <code>Optional|
|**Definition**           |Free text description of the related URL.|
|**Format**               |Free text|
|**Additional Instructions**|      |
|**Examples**             |DOI for related published data|

