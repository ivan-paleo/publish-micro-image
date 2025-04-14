
<!-- TOC ignore:true -->

# Template ZEISS optical microscopes

By Ivan Calandra

<!-- TOC ignore:true -->

# Table of content

<!-- TOC -->

- [Template ZEISS optical microscopes](#template-zeiss-optical-microscopes)
- [Table of content](#table-of-content)
- [Introduction](#introduction)
- [What and how to report](#what-and-how-to-report)
    - [Method section of a paper](#method-section-of-a-paper)
        - [Commons](#commons)
        - [Widefield documentation](#widefield-documentation)
        - [Confocal topography](#confocal-topography)
        - [Correlative imaging](#correlative-imaging)
        - [Pre-processing](#pre-processing)
    - [Data & Metadata](#data--metadata)
        - [General](#general)
        - [Widefield images](#widefield-images)
        - [Topography & surface texture analysis data](#topography--surface-texture-analysis-data)
        - [Correlative imaging](#correlative-imaging)

<!-- /TOC -->



# Introduction

This template explain what I think is important to report and how to report this information for images acquired with any of the ZEISS optical microscopes (stereo-, light, digital or confocal microscopes), using either ZEN core, ZEN blue or Smartzoom software packages.  
The template is meant as an **easy and quick way to report extensive information (metadata) about microscope images**.

This template is split into two parts:

1. What to report in the method section of a paper
2. How to report all necessary metadata together with the data

In the first part, I provide a "fill-in-the-blanks" text that can be pasted into the method section of a paper. In the second, I will show that extensive metadata can be reported and shared without any effort, when the data are shared in appropriate formats.

While this template is specifically targeted at images from the ZEISS light microscopes, I believe that it can be adapted quite easily for images acquired with other optical microscopes (feel free to [contribute](/README.md#how-to-contribute)!).

This template is available as a markdown file (this file) as well as a [DOCX file](/Guidelines/ZEISS_Optical-microscopes.docx).

<br>

# What and how to report
Sample preparation is a very important part of any documentation/observation/analysis. I nevertheless left it out here because it is a whole topic in itself. Here, I mention only the information that need to be reported about the microscope images themselves.  
Many settings are important (see [Minimum Reporting Requirements in the README](/README.md#minimum-reporting-requirements)) but only a few should be reported in the method section of a paper; the rest must be reported but not necessarily in the method.

These recommendations follow and adapt the Bare Minimal Microscopy Reporting Requirements Checklist (Montero Llopis et al. 2025; see [reference in the README](/README.md#references)).


## Method section of a paper
I suggest to use the following text snippets. Parts in square brackets must be adjusted using the text within the brackets as examples or list to choose from. The rest of the text should of course also be adapted to the study.  

Settings and their values can alternatively be presented as tables, either in the main text (recommended) or as supplementary material. The report(s), or parts of it (them), from the Shiny App [imaging-reports](https://github.com/ivan-paleo/imaging-reports) can be used for this. 

### Commons
"[*Objects* or *Features*] were documented with a [*stereo-*, *light*, *digital* or *confocal*] microscope [manufacturer, model, upright/inverted] in [*reflected* or *transmitted*] light at the IMPALA, using the [objective(s) manufacturer and name(s) including nominal magnification(s) and numerical aperture(s), and potentially the working distance, if relevant].  
Each image represents [field of view, e.g. *350 x 350*] µm for [e.g. *2048 x 2048*] pixels, leading to an effective image pixel size of [e.g. *0.17*] µm. The Nyquist criterion was therefore [*fulfilled* or *not fulfilled*; if the latter explain why not].  
The acquisitions were done using the software [name, manufacturer, verion, modules].  
All data in original formats, together with their metadata (acquisition and analysis settings), can be found on Zenodo ([*DOI*])."

All images must have a scale bar!

### Widefield documentation
"[*Brightfield*, *Darkfield*, *Polarized*, etc.] [*EDF*, *stitched*, etc.] images were acquired with the [manufacturer and model] camera. Exposure time was set to [e.g. *30*] ms. "

If z-stacks were acquired:  
"Z-stacks were acquired with the Z-step size set to [e.g. *1*] µm and a total range of [e.g. *30-40*] µm. The Nyquist criterion was therefore [*fulfilled* or *not fulfilled*; if the latter explain why not]."

See [https://doi.org/10.1016/j.jasrep.2023.103869](https://doi.org/10.1016/j.jasrep.2023.103869) for an example.

### Confocal topography
"The system was turned on at least one hour before starting acquisition, so that
all components were warmed up to limit thermic drift.  
A violet laser (405 nm) was used for acquisition. The pinhole was set to 1 Airy Unit.  
Z-stacks were acquired with the Z-step increment set to [e.g. *1*] µm and a total range of [e.g. *30-40*] µm. "

See [https://doi.org/10.1038/s41598-019-42713-w](https://doi.org/10.1038/s41598-019-42713-w) for an example.

### Correlative imaging
"The coordinate system was calibrated with the [objective(s) manufacturer and name(s) including nominal magnification(s) and numerical aperture(s)] objective on the [*digital microscope* and/or *light/confocal microscope*]."  

If you also used SEM for correlative imaging, refer to the guidelines [there](/Guidelines/ZEISS_EVO25.md#correlative-imaging).

See [https://doi.org/10.1038/s41598-024-70265-1](https://doi.org/10.1038/s41598-024-70265-1) for an example.

### (Pre-)processing
Also add details about image processing: e.g. about EDF/stitching (widefield), topography application, and alignment (correlative imaging). See recommendations in the repo's [README](/README.md#processing).

<br>

## Data & Metadata

### General
The data should be uploaded on an open repository (e.g. Zenodo) in original formats to preserve the metadata as well as in open formats for reusability. Add a README file (in TXT format) to the upload.  

Follow the instructions in the how-to's to [upload to Zenodo](/How-tos/Zenodo.md) and to [read CZI files with ImageJ/Fiji](/How-tos/ImageJ2-Fiji.md).

Even though many settings are included in the files as metadata, some of these settings should also be listed in the main text (see [Method section of a paper](#method-section-of-a-paper)).

### Widefield images
- Upload the full-resolution, uncompressed images in CZI format (Zeiss' original and open format). It is recommended to share the pre-processed (e.g. EDF, stitched) images because of the size of the raw images (especially z-stacks). 
- Also upload the overview/preview images showing the location of images on the object. Alternatively, share the CZI files of the images calibrated with Shuttle-and-Find (correlative imaging).
- Specify in the README (in TXT format): "[*Raw* or *Pre-processed*] images were acquired with the software [*ZEN core*, *ZEN blue*, or *Smartzoom*] [version number] from Zeiss. All metadata (acquisition settings) are included in the CZI-files and can be retrieved using e.g. the Bio-Formats plugin for ImageJ/Fiji ([https://docs.openmicroscopy.org/bio-formats/5.8.2/users/imagej/installing.html](https://docs.openmicroscopy.org/bio-formats/5.8.2/users/imagej/installing.html)) or Zeiss ZEN software ([https://www.zeiss.com/microscopy/en/products/software/zeiss-zen.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen.html)). Instructions to do so in ImageJ/Fiji are given here: [https://github.com/ivan-paleo/publish-micro-image/blob/main/How-tos/ImageJ2-Fiji.md](https://github.com/ivan-paleo/publish-micro-image/blob/main/How-tos/ImageJ2-Fiji.md)."

### Topography & surface texture analysis data
- Upload MNT files of the surface texture analysis with Mountains.
- Alternatively or complementarily, upload the SUR files resulting from the topography analysis in ZEN. SUR files can also be exported from Mountains; in that case, be sure to select the uncompressed SUR format.
- Export the MNT files to PDF and upload them too.
- Specify in the README (in TXT format): "Height maps were acquired with the software ZEN blue [version number] from Zeiss. Each surface has been processed in batch with a template in ConfoMap v. [8.2.10044] (a derivative of MountainsMap by Digital Surf, [https://www.digitalsurf.com/software-solutions/profilometry/](https://www.digitalsurf.com/software-solutions/profilometry/)). The result of the analysis on each surface is saved in MNT format (including all original and processed surfaces, their metadata, as well as results) and exported to a PDF file. Ultimately, the results are collated into CSV file(s)."

See [https://doi.org/10.5281/zenodo.6645445](https://doi.org/10.5281/zenodo.6645445) for an example (although the information was added as a description rather than a README file).

### Correlative imaging
- Upload ZEN Connect project(s) (project-name.a5proj).
- Upload images as CZI, ideally in the ZEN connect data folder (project-name_data).
- Optionally, upload the image export(s) as PNG.
- Specify in the README (in TXT format): "ZEN Connect projects for correlative imaging were created with Zeiss' ZEN desk v. [*3.5*] (blue edition, [https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-desk.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-desk.html)) software with the module ZEN Connect ([https://www.zeiss.com/microscopy/en/products/software/zeiss-zen/zen-connect-toolkit.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen/zen-connect-toolkit.html))."

If you also used SEM for correlative imaging, refer to the guidelines [there](/Guidelines/ZEISS_EVO25.md#correlative-imaging-1).