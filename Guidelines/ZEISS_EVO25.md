
<!-- TOC ignore:true -->
# Template ZEISS EVO 25

By Ivan Calandra

<!-- TOC ignore:true -->
# Table of content

<!-- TOC -->

- [Introduction](#introduction)
- [What and how to report](#what-and-how-to-report)
    - [Method section of a paper](#method-section-of-a-paper)
        - [Commons](#commons)
        - [SEM documentation](#sem-documentation)
        - [EDS measurements](#eds-measurements)
        - [Correlative imaging](#correlative-imaging)
    - [Data & Metadata](#data--metadata)
        - [General](#general)
        - [SEM images](#sem-images)
        - [EDS data](#eds-data)
        - [Correlative imaging](#correlative-imaging)

<!-- /TOC -->



# Introduction

This template explain what I think is important to report and how to report this information for scanning electron microscope (SEM) images acquired with the ZEISS EVO 25.  
The template is meant as an **easy and quick way to report extensive information (metadata) about microscope images**.

This template is split into two parts:

1. What to report in the method section of a paper
2. How to report all necessary metadata together with the data

In the first part, I provide a "fill-in-the-blanks" text that can be pasted into the method section of a paper. In the second, I will show that extensive metadata can be reported and shared without any effort, when the data are shared in appropriate formats.

While this template is specifically targeted at images from the ZEISS SEM, I believe that it can be adapted quite easily for images acquired with other SEMs (feel free to [contribute](/README.md#how-to-contribute)!).

This template is available as a markdown file (this file) as well as a [DOCX file](/Guidelines/ZEISS_EVO25.docx).

  
<br> 

# What and how to report
Sample preparation is a very important part of any documentation/observation/analysis. I nevertheless left it out here because it is a whole topic in itself. Here, I mention only the information that need to be reported about the SEM images themselves.  
Many settings are important (see [Minimum Reporting Requirements in the README](/README.md#minimum-reporting-requirements)) but only a few should be reported in the method section of a paper; the rest must be reported but not necessarily in the method.


## Method section of a paper
I suggest to use the following text snippets. Parts in square brackets must be adjusted using the text within the brackets as examples or list to choose from. The rest of the text should of course also be adapted to the study.  
Settings and their values can alternatively be presented as tables, either in the main text (recommended) or as supplementary material. The report(s), or parts of it (them), from the Shiny App [imaging-reports](https://github.com/ivan-paleo/imaging-reports) can be used for this.  

See [https://doi.org/10.1016/j.jasrep.2024.104572](https://doi.org/10.1016/j.jasrep.2024.104572) for an example. 

### Commons
"[*Objects*] were documented by [*SEM* and/or *EDS*] at the IMPALA. The objects were [*uncoated* or *coated with...*].  
All data in original formats, together with their metadata (acquisition and analysis settings), can be found on Zenodo ([*DOI*])."

All images must have a scale bar!

### SEM documentation
"The [*secondary electron* and/or *back-scattered electron*] detector[s] ([*VPSE G4*, *SE1* and/or *HDBSD*]) were used on a [Zeiss EVO 25] at [*low* or *high*] vacuum ([e.g. *30*] Pa) and with an acceleration voltage of [e.g. *10*] kV.  
The acquisitions were done using the software [*Zeiss SmartSEM v6.08* or *Zeiss SmartSEM Touch v2.01*]."

### EDS measurements
Note that EDS measurements must always be accompanied by an SEM documentation, usually using the BSD. 

"The elemental composition was measured by energy-dispersive X-ray spectrometer (EDX, Bruker Quantax XFlash 6|30 M) at [*low* or *high*] vacuum ([e.g. *~0.01*] Pa) and acceleration voltage [e.g. *20*] kV.  
The acquisitions were done using the software [*Bruker Esprit v2.3.0.997*]."

### Correlative imaging
"The coordinate system was calibrated at 150x magnification using the software [*Zeiss ZEN SEM v3.5*]."

If you also used optical microscopes for correlative imaging, refer to the guidelines [there](/Guidelines/ZEISS_Optical-microscopes.md#correlative-imaging).


<br>


## Data & Metadata
### General
The data should be uploaded on an open repository (e.g. Zenodo) in original formats to preserve the metadata as well as in open formats for reusability. Add a README file (in TXT format) to the upload.  

Follow the instructions in the how-to's to [upload to Zenodo](/How-tos/Zenodo.md) and to [read CZI or TIFF files with ImageJ/Fiji](/How-tos/ImageJ2-Fiji.md).

Even though many settings are included in the files as metadata, some of these settings should also be listed in the main text (see [Method section of a paper](#method-section-of-a-paper)).  

See [https://doi.org/10.5281/zenodo.10074758](https://doi.org/10.5281/zenodo.10074758) for an example.

### SEM images
- Upload the full-resolution, uncompressed and unedited SEM images in TIF format.
- Also upload the overview images (*_registration.png) showing the location of images on the object (red rectangle).
- Specify in the README (in TXT format): "SEM images were acquired with the software [*SmartSEM v.6.08* or *SmartSEM Touch v2.01*] from Zeiss ([https://www.zeiss.com/microscopy/en/products/software/zeiss-smartsem.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-smartsem.html)). All metadata (acquisition settings) are included in the TIFF-files and can be retrieved using e.g. the IMBalENce plugin for ImageJ/Fiji ([https://imagej.net/plugins/imbalence](https://imagej.net/plugins/imbalence)). Instructions to do so are given here: [https://github.com/ivan-paleo/publish-micro-image/blob/main/How-tos/ImageJ2-Fiji.md](https://github.com/ivan-paleo/publish-micro-image/blob/main/How-tos/ImageJ2-Fiji.md)."

### EDS data
- Upload the project files in original Bruker format (RTX), except if you only have hypermaps.
- Upload hypermaps files in original Bruker format (BCF) if applicable.
- Export all spectra, including the map's sum spectrum if applicable, to XLSX and upload them.
- Save BSD images, showing the location of EDS spectra for each measurement point in case of measurements in the Objects workspace, in PNG format and upload them. These should be the same images as the BSD images from the SEM but at lower resolution and with less metadata.
- Save all charts of the quantified spectra, including the map's sum spectrum if applicable, in PNG format and upload them.
- Export all quantified results of the spectra, and of the map's sum spectrum if applicable, to XLSX and upload the files.
- Export the quantified map images in PNG format, if applicable, and upload them.
- Specify in the README (in TXT format):
  - "EDS data were acquired and processed with the software Esprit v. 2.3.0.997 from Bruker ([https://www.bruker.com/en/products-and-solutions/elemental-analyzers/eds-wds-ebsd-SEM-Micro-XRF/software-esprit-family.html](https://www.bruker.com/en/products-and-solutions/elemental-analyzers/eds-wds-ebsd-SEM-Micro-XRF/software-esprit-family.html))."
  - "The individual spectra were exported to XLSX format for compatibility. The amount of metadata is limited."
  - Explain what each data type is.
  - Detail the quantification method (alternatively in the method).

### Correlative imaging
- Upload ZEN Connect project(s) (project-name.a5proj).
- Upload images as CZI and/or TIF, ideally in the ZEN connect data folder (project-name_data).
- Optionally, upload the image export(s) as PNG.
- Specify in the README (in TXT format): "ZEN Connect projects for correlative imaging were created with Zeiss' ZEN desk v. [*3.5*] (blue edition, [https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-desk.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-desk.html)) software with the module ZEN Connect ([https://www.zeiss.com/microscopy/en/products/software/zeiss-zen/zen-connect-toolkit.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen/zen-connect-toolkit.html))."

If you also used optical microscopes for correlative imaging, refer to the guidelines [there](/Guidelines/ZEISS_Optical-microscopes.md#correlative-imaging-1).
