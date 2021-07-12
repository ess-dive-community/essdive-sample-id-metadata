# ESS-DIVE Sample ID and Metadata Reporting Format (IGSN-ESS) v1.1.0

ESS-DIVE recommends registering samples for [Global Sample Numbers (IGSNs)](https://www.igsn.org/) through the [System for Earth Sample Registration (SESAR)](https://www.geosamples.org/). IGSNs are associated with standardized metadata to characterize a variety of different samples and their collection details. These sample identifiers facilitate sample discovery, tracking, and reuse; they are especially useful when sample data is shared with collaborators, sent to different labs or user facilities for analyses, or distributed in different data files, datasets, and/or publications. 

ESS-DIVE has worked with our community scientists to test use of IGSNs and associated metadata in interdisciplinary Environmental Systems Science (ESS). Here we outline modified IGSN metadata guidelines to account for needs of a variety of related geological and biological samples. While generally following the IGSN core descriptive metadata schema, we provide recommendations for extending sample type terms, and connecting to related templates geared towards biodiversity (Darwin Core) and genomic (Minimum Information about any Sequence, MIxS) samples and specimens. The resulting template and recommendations are an extension of IGSN core metadata - IGSN for Environmental Systems Science (IGSN-ESS). 

## Getting started

[ESS-DIVE's IGSN metadata reference guide](guide.md): <br>IGSN sample metadata guide, modified (from the SESAR IGSN guide - see link and citation below) for interdiscipinary Environmental System Science (ESS) samples. 

Other documents to get started:
- [Instructions document](instructions.md): Instructions to register samples for IGSNs through SESAR, and submit related datasets to ESS-DIVE. 
- [Sample metadata template](sampleTemplate.xls): Download spreadsheet template with standard fields to register samples for IGSNs. 

## Updates in v1.0.0  
- This is the second release of the Sample ID and Metadata Reporting Format  

## File formatting requirements

ESS-DIVE has higher-level requirements and recommendations for documenting individual files, including those in csv spreadsheet formats.  Here is a quick summary of relevant requirements. 

- File names should include only ASCII characters, camelCase, underscores or dashes.
- There should be no empty rows.
- Reporting should be consistent within a column, for example with the same number of decimal places where relevant. 
- Use "NA" for missing values in columns with text, and "-9999" for missing values in columns with numbers. 


## How to contribute: 

Want to make a change to the reporting format? [Submit a new issue](https://github.com/ess-dive-community/essdive-sample-id-metadata/issues/new/choose) and use one of several templates that we provide to: suggest a new term, modify a term, or propose changes to documentation within this repository.

Have a question? Contact us at ess-dive-support@lbl.gov. 

The issue templates we use are modeled from that provided by Darwin Core: 

Darwin Core maintenance group, Biodiversity Information Standards (TDWG) (2014). Darwin Core. Zenodo. https://doi.org/10.5281/zenodo.592792   

---
## About the sample ID and metadata reporting format

The ESS-DIVE sample ID and metadata reporting format primarily follows the SESAR IGSN guide and template, with modifications to address ESS sample needs and practicalities. To develop recommendations for ESS, we conducted research on related sample standards and templates in addition to work with project scientists to test use of IGSN and standard metadata. See our related paper describing the recommended sample ID and metadata reporting format: http://doi.org/10.5334/dsj-2021-011. 

Below we outline supporting documents used to compare related metadata and vocabulary terms.  

[Metadata research documents](/terms): Files with descriptions of metadata fields and controlled vocabulary terms. Metadata fields with controlled vocabularies are described in the [sample metadata reference guide](guide.md). 

- [Sample metadata translation table](/terms/sampleMetadataTranslationTable.csv): Comparison of basic sample metadata elements across standards and templates to describe physical samples and specimens. 
- [Sample metadata sources](/terms/sampleMetadata_sources.md): List of sources for standard or template in translation table, with scope and available citation. 
- [Object type vocabulary](/terms/objectType.md): Description of terms for ESS-DIVE IGSN sample object types. 
  * [Object type comparison](/terms/objectType_translation_table.csv): Comparison of object type terms.
- [Material vocabulary](/terms/material.md): Description of terms for ESS-DIVE IGSN sample object types. 
  * [Material comparison](/terms/material_translation_table.csv): Comparison of material terms. 
- [Units vocabulary](/terms/units.md): Subset of likely relevant units terms from the [Units Ontology (UO)](http://www.ontobee.org/ontology/UO).

## Copyright information
The ESS-DIVE Sample ID and metadata reporting format (IGSN-ESS) is licensed under the Creative Commons Attribution 4.0 International (CCby4).

## Funding and acknowledgements

Funding for the development of ESS-DIVE's Sample ID and metadata reporting format was provided by the US Deparment of Energy (DOE), Biological and Environmental Research Program, Earth and Environmental Systems Sciences Division, Data Management.

The updated sample reporting format for interdisciplinary ESS samples contains modifications and extensions of guidelines originally created by the System for Earth Sample Registration (SESAR) and IGSN organization. Individuals within these organizations are responsible for creating IGSN identifiers and standard sample metadata templates. We especially thank Kerstin Lehnert, Jens Klump, Lesley Wyborn, and Sarah Ramdeen for their development and engagement work, and/or direct assistence with using IGSN. 

As outlined in the [sample metadata sources](/terms/sampleMetadata_sources.md) document, many recommended metadata additions to the IGSN guidelines/schema come from Darwin Core, and MIxS. We utilize formats for our user guides from [Darwin Core resources](https://github.com/tdwg/dwc), as well.  

ESS community scientists helped test use of IGSNs, and provided critical feedback - resulting in our final recommendations. These include individuals from eight ESS projects, including: 
- SLAC Subsurface Biogeochemical Research (SBR) Scientific Focus Area (SFA), National Accellerator Laboratory Groundwater Quality: Zach Perzan and Kristin Boye
- Lawrence Livermore National Lab SBR SFA, Subsurface Biogeochemistry of Actinides: Nancy Merino and Mavrik Zavarin
- Pacific Northwest National Lab SBR SFA, Worldwide Hydrobiogeochemistry Observation Network for Dynamic River Systems (WHONDRS): Amy Goldman and James Stegen
- Argonne National Lab SBR SFA, Argonne Wetland Hydrobiogeochemistry: Pamela Weisenhorn 
- Lawrence Berkeley National Lab SBR SFA, Watershed Function (2 sub-projects): Patrick Sorensen, Dana Chadwick, Zarine Kakalia, Eoin Brodie
- Lawrence Berkeley National Lab Terrestrial Ecosystem Function (TES) SFA, Belowground Biogeochemistry
- Next Generation Ecosystem Experiments -Arctic (NGEE-Arctic) and -Tropics (NGEE-Tropics) projects: Kim Ely

We thank representatives from other US DOE data systems and user facilities that work with ESS samples who have contributed to sample discussions, including: 
- Joint Genome Institute (JGI): Kjiersten Fagnan, David Hays
- National Microbiome Data Collaborative (NMDC): Emiley Eloe-Fadrosh, Elisha Wood-Charlson, Chris Mungall, William Duncan
- The Department of Energy Systems Biology Knowledgebase (KBase): Shane Canon, Paramvir Dehal
- Environmental Molecular Sciences Laboratory: Lee Ann McCue, Dave Millard, Steven Wiley

## Recommended citation

_**Please cite the SESAR IGSN guide and/or schema, Darwin Core, and ESS-DIVE's modified version for Environmental Systems Science Samples when describing sample collection and data management methods in your related datasets and publications.**_ 

System for Earth Sample Registration (SESAR). 2020. SESAR Batch Registration Quick Guide (Version 7.0). Zenodo. http://doi.org/10.5281/zenodo.3874923

System for Earth Sample Registration (SESAR). 2020. SESAR XML Schema for samples (Version 4.0). Zenodo. http://doi.org/10.5281/zenodo.3875531 

Darwin Core maintenance group, Biodiversity Information Standards (TDWG) (2014). Darwin Core. Zenodo. https://doi.org/10.5281/zenodo.592792   

Damerow J ; Varadharajan C ; Boye K ; Brodie E ; Burrus M ; Chadwick D ; Cholia S ; Crystal-Ornelas R ; Elbashandy H ; Eloy Alves R ; Ely K ; Goldman A ; Hendrix V ; Jones C ; Jones M ; Kakalia Z ; Kemner K ; Kersting A ; Maher K ; Merino N ; O'Brien F ; Perzan Z ; Robles E ; Snavely C ; Sorensen P ; Stegen J ; Weisenhorn P ; Whitenack K ; Zavarin M ; Agarwal D  (2020): Sample Identifiers and Metadata Reporting Format for Environmental Systems Science. Environmental Systems Science Data Infrastructure for a Virtual Ecosystem (ESS-DIVE). https://doi.org/10.15485/1660470
