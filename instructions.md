# ESS-DIVE Instructions to Register Samples for IGSNs

General information about International Geo/General Sample Numbers (IGSNs) can be found on the [System for Earth Sample Registration (SESAR) website.](https://www.geosamples.org/igsnabout) 

ESS-DIVE has been testing use of IGSN for the U.S. Department of Energy’s Environmental System Science (ESS) community, and has begun outlining recommended modifications to SESAR IGSN terms and some additional metadata fields to include for this community. 

Here are instructions on how to register your ESS samples for IGSNs through SESAR, and submit your sample metadata and data to ESS-DIVE. 

1. Register and login to [SESAR's geopass system](http://geopass.iedadata.org/josso/), and select a user code. The user code should generally be specific to an individual or project. You should use the same user code for all current and future samples. This is important to a.) effectively manage your sample metadata over time (e.g. add links to related publications), and b.) avoid the proliferation of user codes.   

2. Plan the allocation of identifiers for your samples and sample relationships. Within the SESAR IGSN metadata template, sample relationships are captured by specifying the “Parent IGSN” for each IGSN registered. Therefore, parent samples must be registered before the child samples. For ESS-DIVE, we are also now using location IDs, sampling event IDs, and/or sample collection IDs (which should be project-specific and unique IDs). These project-specific IDs can be described in separate files and submitted along with your ESS-DIVE data packages associated with the samples. An example sample “journey map” (documenting sample transport, analyses, and relationships) may help you map out your general sample relationships and decide on the allocation of IDs. 

Many projects involved in our testing have expressed a preference to use identifier extensions for highly-related subsamples (e.g. containers sent for multiple analyses that represent a particular sample); You can assign short 1-2 character extensions for subsamples by specifying your own IGSNs and registering those subsamples along with relevenat metadata.

3. Fill out a customized [sample template for ESS-DIVE](sampleTemplate.xls). General fields to describe sample types and locations are required where relevant. Guidance on specific fields were originally developed by SESAR, and modified in some cases by ESS-DIVE. See our [sample metadata guide](guide.md) for descriptions and instructions for each metadata field. 

Some projects may choose to register samples that have already been collected and analyzed. We are developing R scripts to help facilitate standardization of existing metadata, and will provide these when completed. 

4. To pre-register samples before sample collection, you can batch upload basic registration metadata (i.e. Object type); this enables the ability to print IGSNs and QR code labels directly from [MySESAR](https://geopass.iedadata.org/josso/). Required metadata to register a sample include the Object type (e.g. individual sample), and project-specific sample names. If the sample was derived from a parent sample, then you also must provide the IGSN for the parent sample. Note that most metadata is not known until sample collection, and would be uploaded later (step 7). If registering samples after collection, you can upload all metadata together, and skip steps 5-6.

5. If desired, print labels from MySESAR by selecting registered samples, note that samples can include a project-specific sample name in addition to the IGSN, as shown in the [example label here](http://www.geosamples.org/help/labelprinting).  

6. Collect samples and metadata in the field.

7. Batch upload completed descriptive metadata for registered samples after field collection in the [customized spreadsheet template](sampleTemplate.xls).

8. Manage and update sample metadata as needed. It is essential that the IGSNs always be associated with all digital records of the sample. However, the SESAR IGSN catalog is focused on fields related to the “birth” of the sample, so data related to analyses would be managed separately, and not included in the SESAR catalog. Instead, updates to SESAR metadata would likely include adding links to related datasets and publications, or updating archive location. 

9. When the relevant sample analyses are completed for a data package, submit your sample metadata and data to [ESS-DIVE](https://data.ess-dive.lbl.gov/). ESS-DIVE will be developing tools to enable advanced search for samples using IGSNs, and linking samples to other related samples, datasets and publications. 

We will continue to work with the ESS community to improve the representation of ESS samples in standard sample metadata relevant across a variety of biological and geological samples. Please [contribute](contribute.md) by submiting issues, using our issue templates, or contact ess-dive-support@lbl.gov to provide any feedback on the process of registering samples for IGSNs, specific metadata fields or controlled vocabulary terms.
#
