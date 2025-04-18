
<!-- TOC ignore:true -->
# Template WAYGATE TECHNOLOGIES Phoenix V|tome|x L

By Ivan Calandra

<!-- TOC ignore:true -->
# Table of content

<!-- TOC -->

- [Introduction](#introduction)
- [What and how to report](#what-and-how-to-report)
    - [Method section of a paper](#method-section-of-a-paper)
    - [Data & Metadata](#data--metadata)
        - [General](#general)
        - [CT data](#ct-data)
        - [CT metadata](#ct-metadata)
        - [README](#readme)

<!-- /TOC -->



# Introduction

This template explain what I think is important to report and how to report this information for X-ray computed tomography (CT) data acquired with the WAYGATE TECHNOLOGIES Phoenix V|tome|x L. Although it is not a microscope, we do have a CT scanner at the IMPALA and I wanted to have such a template for this instrument as well.  
  
The template is meant as an **easy and quick way to report extensive information (metadata) about CT data**.

This template is split into two parts:

1. What to report in the method section of a paper
2. How to report all necessary metadata together with the data

In the first part, I provide a "fill-in-the-blanks" text that can be pasted into the method section of a paper. In the second, I will show that extensive metadata can be reported and shared without any effort, when the data are shared in appropriate formats.

While this template is specifically targeted at images from the Phoenix V|tome|x, I believe that it can be adapted quite easily for images acquired with other CTs (feel free to [contribute](/README.md#how-to-contribute)!).

This template is available as a markdown file (this file) as well as a [DOCX file](/Guidelines/WAYGATE_VtomexL.docx).
  
<br> 

# What and how to report
Sample preparation is a very important part of any documentation/observation/analysis. I nevertheless left it out here because it is a whole topic in itself. Here, I mention only the information that need to be reported about the CT data themselves.  
Many settings are important but only a few should be reported in the method section of a paper; the rest must be reported but not necessarily in the method.


## Method section of a paper
I suggest to use the following text snippets. Parts in square brackets must be adjusted using the text within the brackets as examples or list to choose from. The rest of the text should of course also be adapted to the study.   

Settings and their values can alternatively be presented as tables, either in the main text (recommended) or as supplementary material. The report(s), or parts of it (them), from the Shiny App [imaging-reports](https://github.com/ivan-paleo/imaging-reports) can be used for this.  

"The objects were scanned with a Phoenix V|tome|x L CT-scanner (Baker Hughes Waygate Technologies) at the IMPALA. The [*microfocus* or *minofocus*] tube was used at [e.g. 110] kV and [e.g. 250] μA, yielding [e.g. 27.5] W. The focal spot size is roughly equal to the power, i.e. [27.5] μm. Voxel size was geometrically set to [e.g. 22] μm. Such values for power and voxel size are in an optimal relationship with each other to ensure adequate levels of geometric unsharpness.  
Acquisitions and reconstructions were performed in datos|x v2.10.1.  
All acquisition and reconstruction settings can be retrieved from the PCA and PCR files, respectively, available for each scan on Zenodo ([*DOI*]). These files can be opened with any text editor."

See [https://doi.org/10.1371/journal.pone.0314039](https://doi.org/10.1371/journal.pone.0314039) for an example.

<br>

## Data & Metadata
### General
The data should be uploaded on an open repository (e.g. Zenodo) in original formats to preserve the metadata as well as in open formats for reusability. Add a [README file](#readme) (in TXT format) to the upload.  

Follow the instructions in the how-to's to [upload to Zenodo](/How-tos/Zenodo.md).

Even though many settings are included in the files as metadata, some of these settings should also be listed in the main text (see [Method section of a paper](#method-section-of-a-paper)).  

### CT data
Due to the size of the 3D models, we do not have a solution yet to share the CT data (individual images or 3D models). Currently, we can only share the PCA and PCR files (see [CT metadata](#ct-metadata) below).  

### CT metadata
Upload PCA and PCR files for every 3D model.  
In case of a multi|scan, upload only the PCA and PCR files from the project folder (= not for each individual scan).

### README
Specify in the README file, in TXT format:

"The scans were acquired with datos|x acquisition v. 2.10.1.21328, reconstructed with datos|x reconstruction v. 2.10.1.21292 (Baker Hughes, [https://www.bakerhughes.com/waygate-technologies/ndt-software/phoenix-datosx-industrial-ct-acquisition-reconstruction-software](https://www.bakerhughes.com/waygate-technologies/ndt-software/phoenix-datosx-industrial-ct-acquisition-reconstruction-software)) and processed with VGSTUDIO MAX v. [3.5.2.release3.5.2-233823-51ca2b7a86c 64 bit] (Volume Graphics [https://www.volumegraphics.com/en/products/vgsm.html](https://www.volumegraphics.com/en/products/vgsm.html)).  
The PCA files include all the acquisition settings automatically generated by datos|x acquisition. The PCR files include all the reconstruction settings automatically generated by datos|x reconstruction. Both types of files can be opened with a text editor.  
Due to the size of the 3D models, only the PCA and PCR files are made available here. 3D models and/or raw data will be made available on request: contact [Name, email]."

See [https://doi.org/10.5281/zenodo.10631628](https://doi.org/10.5281/zenodo.10631628) for an example.
