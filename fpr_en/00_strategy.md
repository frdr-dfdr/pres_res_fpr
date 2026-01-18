# Digital Preservation Services File Format Strategy
Last updated: 2025-12-09

Understanding file formats is integral to implementing strategies that aid in the continued access and reuse of research data. This page contains information about digital preservation services file format work. This page will be updated as we develop our strategy. 

For additional information about Digital Preservation Services at the Digital Research Alliance of Canada, please visit the [digital preservation services page](https://github.com/Alliance-RDM-GDR/Digital_Preservation_Services).

## Strategy
While repositories may provide a list of recommended formats we recognize that not all research projects can use openor recommended file formats. Therefore, all file formats are accepted. Different preservation levels are implemented to determine digital preservation capabilities for the various file formats received. 

### Preservation Levels

| Action | Basic level | Watch Level | Full Level|
| :----------- | :-----------: | :-----------: | :-----------: |
| Regular fixity checks | ✔️ | ✔️ | ✔️ |
| Virus scanning  | ✔️ | ✔️ | ✔️ |
| Geo-redundant storage | ✔️ | ✔️ | ✔️ |
| Storage refresh/replace | ✔️ | ✔️ | ✔️ |
| File format identification | ✔️ | ✔️ | ✔️ |
| Generation of preservation metadata |  | ✔️ | ✔️ |
| Watch format for ability to preserve  |  | ✔️ | ✔️ |
| Perform normalization (file migration)  |  | | ✔️ |
| Long-term storage in preservation format  |  | | ✔️ |
| Monitor format over time |  | | ✔️ |

- Adapted from Simon Fraser University, Archives and Records Management, Format Policy Registry
  
#### Basic Level
Basic level of preservation, the bit-stream (1s and 0s) of the file are preserved. No file migration or normalization occurs at this level. Basic level includes:
- File identification, when possible
- Fixity checks
- Store two complete copies of the digital files in different geographic locations
- Virus checking

The basic level of preservation cannot ensure that the file can be rendered in the future.

#### Watch Level 
Watch level includes files that are proprietary but are prevalent in the industry that the likelihood of obsolescence is unlikely. The watch level includes all elements of basic level with the additional preservation activities:
- Monitoring of the formats
- Generation of metadata for preservation and access

#### Full Level 
Full level includes files that the repository has confidence will be available in the long term because they are commonly used, the formats are open and documented, or the formats can be normalized to a preservation friendly format. Full level preservation includes all actions undertaken at the basic and watch level with the additional preservation activities:
- Normalization of file formats to preservation friendly formats
- File format identification
- File format validation
- Monitoring of format

The team is currently working on a develoing a list for researchers outlining which file formats fall into which categories.

## Digital Preservation Activities
### Fixity Checking
Fixity determines whether or not a digital file has been altered or changed. Establishing fixity is a method for ensuring the integrity of files.

### File Format Identification
File format identification involves determining the version and the specific type of a file. [Siegfried](https://github.com/richardlehane/siegfried) is used for file format identification work. [DROID](https://www.nationalarchives.gov.uk/information-management/manage-information/preserving-digital-records/droid/) is used for testing file format signatures.

### File Format Validation
File format validation involves checking if a file format conforms to its file format specification. 

### File Format Characterization
File format characterization involves extracting metadata from the file. The metadata may include information such as aspect ratio or compression level.

### Normalization
An activity that results in digital objects of a particular type converted to a single chosen file format that are non-proprietary and designated preservation friendly. Example jpg, png, gif are normalized to tiff.

### Original Files
In all instances, digital preservation services keeps the original files as it holds information that the derivatives will not contain.

## Storage
Different storage options are employed to achieve digital preservation activities. These include:
- Level 1: Two complete copies of the files in the dataset stored in two different geographic locations. 
- Level 2: Three complete copies of files in the dataset with one copy on a different storage media type. 
- Level 3: Three complete copies of the files in the dataset, one copy stored in a different location with a different disaster threat level.
  
## File Format Risk Matrix - Forthcoming
---
The Digital Research Alliance of Canada develops [file format signatures](https://drive.google.com/drive/folders/1ZHI51Nnb_yAqfIatL7rdSqwHTUGLkSJk) for the inclusion in PRONOM maintained by The National Archives of the United Kingdom (TNA).

---
## Acknowledgements
The file format strategy and the format policy registry (fpr) draws on the excellent work being undertaking internationally by libraries, archives, galleries, museums and repositories including but not limited to

- [Archives and Records Management, Simon Fraser University](https://www.sfu.ca/archives.html)
- [DANS (Data Archiving and Records Service)](https://dans.knaw.nl/en/)
- [Library and Archives Canada](https://www.canada.ca/en/library-archives/services/government/information-disposition/management/guidelines/file-formats-transfer.html)
- [Library of Congress, Sustainability of Digital Formats](https://www.loc.gov/preservation/digital/formats/)
- [National Archives and Records Administration (NARA), Digital Preservation](https://github.com/usnationalarchives/digital-preservation)

Thank you for all your work!
