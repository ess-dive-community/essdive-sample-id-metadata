# How to Assign Sample Identifiers and Register Samples for IGSNs

- [File Organization and Assigning Unique Identifiers](#file-organization-and-assigning-unique-identifiers)     
- [Sample Hierarchies](#sample-hierarchies)
- [Standardize Sample Metadata](#standardize-sample-metadata)
- [When do you need IGSNs?](#when-do-you-need-igsns) 
- [Register Samples for IGSNs through SESAR](#register-samples-for-igsns-through-sesar) 
- [Publish Sample Datasets on ESS-DIVE](#publish-sample-datasets-on-essdive) 
- [Provide Feedback](#provide-feedback) 


## File Organization and Assigning Unique Identifiers

The first step in planning your sampling campaign is to decide how to organize information about your samples, which includes considering file organization and linking or tracking information using unique identifiers. A common way to organize sample data, is to have separate files for locations (project sites), primary samples, and potentially subsamples; each location, sample, and subsample then get a unique identifier (e.g. Location ID, Sample Name). Your locally-unique sample identifiers are called "Sample Name" in the ESS-DIVE sample ID and metadata reporting format, based on SESAR IGSN. The Sample Name is usually a meaningful code that enables you to organize and track samples within your project (e.g. RockCr001_2021-05-25). 

Consistently using unique identifiers for locations, sample collections, sampling events, samples, and subsamples will enable you to efficiently link related information across files (e.g. not input the same latitude and longitude across your sample set). 

## Sample Hierarchies

You may have complex sample hierarchies, and this can be captured in the sample metadata template by providing the Parent IGSN for each subsample (child sample). An example [sample “journey map”](http://bit.ly/SampleJourneyMap) (documenting sample transport, analyses, and relationships) or [sample hierarchy](https://bit.ly/SampleHierarchy) may help you map out your general sample relationships and decide on the allocation of IDs.

When sending a sample to multiple labs for a variety of analyses that need to be later compiled, we recommend using the same identifier for each container, or using extensions from a primary ID to simplify sample reporting and tracking. You can assign short 1-2 character extensions for subsamples by specifying your own IGSNs and registering those subsamples along with relevant metadata.

## Standardize Sample Metadata

Complete the [sample template](https://github.com/ess-dive-community/essdive-sample-id-metadata/blob/master/sampleTemplate.xls) for ESS-DIVE to provide information about samples that will help make them more discoverable and usable. General fields to describe sample types and locations are required where relevant. Guidance on specific fields were originally developed by SESAR, and modified in some cases by ESS-DIVE. See our [sample metadata guide](https://github.com/ess-dive-community/essdive-sample-id-metadata/blob/master/guide.md) for descriptions and instructions for each metadata field.

## When do you need IGSNs

International Geo/General Sample Numbers (IGSNs) are globally unique and persistent identifiers (PID). General information about International Geo/General Sample Numbers (IGSNs) can be found on the [System for Earth Sample Registration (SESAR) website](https://www.geosamples.org/igsnabout).

Each IGSN is associated with a persistent landing page (e.g. [IEWFS0001](https://app.geosamples.org/sample/igsn/IEWFS0001), [10.58052/IEWFS00IX](https://app.geosamples.org/sample/igsn/10.58052/IEWFS00IX)) that contains both human and machine-readable, sample-specific metadata that characterizes the sample type and how, when, why, and where the sample was collected. This landing page can be used to discover related samples and data, and to link and exchange information about the sample.  

IGSNs will likely be most useful for projects where samples will be:
* Used within multiple datasets and journal publications
* Sent to numerous collaborators who work on the same samples
* Sent to multiple labs for analyses
* Published in different data systems or repositories
* Used for multiple purposes over time

## Register Samples for IGSNs through SESAR

Here are instructions on how to register your ESS samples for IGSNs through SESAR.

1. Sign-up and login to SESAR's geopass system, and select a user code. The user code should generally be specific to an individual or project. You should use the same user code for all current and future samples. This is important to a.) effectively manage your sample metadata over time (e.g. add links to related publications), and b.) avoid the proliferation of user codes.
2. Plan the allocation of identifiers for your samples and sample relationships (see Sample Hierarchies section above). Within the SESAR IGSN metadata template, sample relationships are captured by specifying the “Parent IGSN” for each IGSN registered. Therefore, parent samples should generally be registered before the child samples. 
3. You can register samples for IGSNs before or after sample collection. To pre-register samples before sample collection, you can batch upload basic registration metadata (i.e. Object type); this enables the ability to print IGSNs and QR code labels directly from MySESAR as shown here. Required metadata to register a sample include the Object type (e.g. individual sample), and project-specific sample names. If the sample was derived from a parent sample, then you also must provide the IGSN for the parent sample. Note that most metadata is not known until sample collection, and would be uploaded later (step 7). If registering samples after collection, you can upload all metadata together in one step.
4. Collect samples and metadata in the field.
5. Batch upload completed descriptive metadata for registered samples after field collection using the customized spreadsheet template.
6. Manage and update sample metadata as needed. It is essential that the IGSNs always be associated with all digital records of the sample. However, the SESAR IGSN catalog is focused on fields related to the “birth” or collection of the sample, so data related to analyses would be managed separately, and not included in the SESAR catalog. 

## Publish Sample Datasets on ESSDIVE

7. When the relevant sample analyses are completed for a data package, submit your sample metadata and data to ESS-DIVE. ESS-DIVE will be developing tools to enable advanced search for samples using IGSNs, and linking samples to other related samples, datasets and publications.
8. Update your sample metadata when datasets are published by adding links to related datasets and publications, as a “Related URL” along with a “URL Description”.

## Provide Feedback

We will continue to work with the ESS community to improve the representation of ESS samples in standard sample metadata relevant across a variety of biological and geological samples. Please [contribute](contribute.md) by submiting issues, using our issue templates, or contact ess-dive-support@lbl.gov to provide any feedback on the process of registering samples for IGSNs, specific metadata fields or controlled vocabulary terms.
#
