# Format Risk Matrix

## Purpose

The format risk matrix outlines the formats in FRDR and assigned a risk level which is derived by answering a series of weighted questions. The risk matrix borrows heavily from NARA’s File Format Risk Matrix. The sections outlined below provide guidance on how to fill in the sheet. 

## Risk Levels

Risk levels are divided into three categories:

| Category | Description |
| :---- | :---- |
| Low 0% \- 25 % | Files are well supported, widely-adopted, and have open stable specifications. |
| Moderate 26% \- 50% | Files pose some challenges but the risks are manageable. |
| High 51% \- 100% | Files pose significant challenges to long-term access and reuse. Factors include lack of documentation, proprietary, or obsolete dependencies. |

### Weighting

The weight system for the risk analysis is as follows

* Yes \= 1  
* No \= 0  
* N/A \= not included in the calculation

The following areas are assigned a multiplier weight depending on the risk associated with a negative answer.

| Category | Multiplier rate | Total Possible Points\* |
| :---- | :---- | :---- |
| Disclosure | Critical \= 3 | 12 |
| Adoption | High \= 2 | 6 |
| Transparency | Standard \= 1 | 4 \*add 3 to the overall maximum totally for binary formats. |
| Self-documentation | Standard \= 1 | 2 |
| External Dependencies | Standard \= 1 | 5 |
| Patents | Standard \= 1 | 2 |
| TPMs | High \= 2 | 4 |

\*Total possible points can change if a risk element is not applicable

### Calculation

Final preservation score % \= (sum of weighted points/total maximum possible weighted points) x 100

Final risk score \= 100% \- Final preservation score

A penalty of 3 points is added to the overall maximum score if the format is binary.

## Resources

* [Sustainability Factors](https://www.loc.gov/preservation/digital/formats/sustain/sustain.shtml) (LoC)	  
* [Danish National Archives \- Concept Model](https://github.com/the-danish-national-archives/concept-model/tree/main/P2%20Format%20Assessment)   
* [https://github.com/usnationalarchives/digital-preservation/tree/full/Digital\_Preservation\_Risk\_Matrix](https://github.com/usnationalarchives/digital-preservation/tree/master/Digital_Preservation_Risk_Matrix)	  
* [https://harvardwiki.atlassian.net/wiki/spaces/digitalpreservation/pages/48136762/Assessment+Tool](https://harvardwiki.atlassian.net/wiki/spaces/digitalpreservation/pages/48136762/Assessment+Tools)

## Matrix Elements and Questions

### Disclosure

Disclosure refers to the degree to which a complete specification of the format exists and is accessible. Specifications that go through external expert evaluation are preferable.

| Question | Description |
| :---- | :---- |
| Is the format open? | Indicate how open the file format is. For example, the file format has an open license or is proprietary and has a restricted license that is owned by a company or individual. Restricted licensing can be linked to preservation challenges including obsolescence and backward compatibility issues. |
| Does the format have a published specification? | Indicate whether the format has an openly published specification. By open it means that the specification is not behind a paywall. |
| **If yes,** is the specification published and approved by a standards organization? | Specifications that have been approved and published by an internationally recognized standards organization have undergone a controlled process for creation and publication. There is a stable mechanism for maintaining the specification. |
| Was the specification updated in the last 5 years? | As formats age, the potential risk increases because they may be superseded by newer formats and software and tool support may decrease. |
| **Multiplier x 3** |  |

### Adoption

Adoption refers to the level in which a format is in use by the community, primary creators and disseminators. The more widely used the format the less likely it will disappear. Tools to mitigate obsolescence such as emulation and migration are more likely to be in place. If the format has been assessed as preferred or acceptable for long-term preservation at other repositories or institutions engaged with long-term preservation work, this also provides evidence of adoption. 

| Question | Description |
| :---- | :---- |
| Is the format used for preservation in the community? | Formats that are used widely by repositories and the larger digital preservation as a preferred preservation formats, are likely to be more stable in the long-term |
| Is the format prevalent within the community/research field? | The more widely used a file format is used in the research field or for research data in general the more likely the file will remain in existence in the long-term. |
| Is the file format actively maintained by the community? | File formats that are maintained by a community rather than one or two individuals are more likely to remain available in the long-term. |
| **Multiplier x 2**|  |

### Transparency

Transparency refers to a format that can be analyzed using basic tools including text-only editors. Transparency is enhanced if metadata is embedded for non-text content in a UNICODE using UTF-8 encoding. Source code is more transparent than compiled code. 

Encryption is incompatible with transparency.

Compression inhibits transparency. If a repository must take in material that is compressed, compression algorithms that are common and widely used are preferred. Lossless would be preferred to lossy compression

| Question | Description |
| :---- | :---- |
| Is the format character-based? | Character-based file formats are human readable, platform-independent and based in a character encoding (ASCII, UTF-8, etc.) |
| Can the file be identified by elements other than the extension?  | File formats that have an internal signature increase the ability of the file to be identified. |
| Is the format uncompressed? | Compressed file formats are used to optimize space and transmission but some compression methods result in permanently removing data from the file. The most common compression methods are known as lossy and lossless. |
| **If yes,** does the format use a compression other than lossy?  | Lossy compression permanently removes data from files. This causes degradation of the data in comparison from its original.|
| **Multiplier x 1** | 

### Self-Documentation

Self-Documentation refers to formats with metadata stored with the digital object that is used to render the digital object. These formats are easier to sustain over time. The ability of the format to hold administrative and technical metadata is an advantage for preservation.

| Question | Description |
| :---- | :---- |
| Does the format natively include metadata that documents the file and the technical environment used to create (and/or modify) it? | Formats that natively include technical metadata about their creation will likely be easier to sustain and provide access to over time. |
| Does the format support adding embedded metadata through manual or automated processes? | Formats that natively support adding embedded descriptive and administrative metadata are more likely to contain information about the context of their creation and the chain of custody, both of which are important for providing meaningful access to records over time. |
| **Multiplier x 1 - override on binary formats add 3** |  |

### External Dependencies

External Dependencies refers to the degree to which the format depends on a particular hardware, software and operating system to be rendered.

The ability to sustain static content is easier than sustaining dynamic content.

| Question | Description |
| :---- | :---- |
| Can the format be used in various hardware environments to be rendered? | If a specific hardware environment needed to render and migrate the file format, if yes, the likelihood of continued access is diminished. |
| Are there many renderers available for the format? | If renderers are not available for the format then there is less likelihood of providing continued access. |
| Is at least one renderer open source? | If renderers are only proprietary then the risk of being able to render the object is put at risk. Older renderers may discontinue support for older versions of the formats as they are updated. |
| Can the format be rendered or executed in multiple computing operating systems? | Formats that cannot be rendered in more than one computing operating system are typically representative of data that is difficult to transfer between computing systems. |
| Is the software that was used to create the format currently supported? | Can the software be deployed using current hardware environments? If not, then a risk to the digital object is present. |
| **Multiplier x 1** |  |

### Impact of Patents {#impact-of-patents}

Impact of Patents refers to the limitations from licenses or patents to decode formats for future use. This will impact the development of open source encoders or decoders that can aid in rendering the digital object.

| Question | Description |
| :---- | :---- |
| Is the format free of patent claims? | Formats subject to patent claims have higher preservation risk associated with them as the ability to manage the formats is tied to a specific software. |
| Does the format have open source license terms? | File formats that have open licenses associated with their usages have a low risk related to usage of the format and the creation of tools to process the format for access and long-term preservation. |
| **Multiplier x 1** |  |

### Technical Protection Mechanisms {#technical-protection-mechanisms}

Technical Protection Mechanisms (TPMs) refers to the ability to replicate digital content on new media, through migration or normalization activities.

| Question | Description |
| :---- | :---- |
| Is the format free of encryption? | Encryption restricts access and creates risks to managing and migrating files in the long-term. |
| Is the format free of technical protection measures? | Similar to encryption, technical protection measures may prevent organizations from rendering the file for validation and processing, and they also inhibit long-term access to the content. |
| **Multiplier x 2** |  |

