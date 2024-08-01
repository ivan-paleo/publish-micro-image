
<!-- TOC ignore:true -->
# Template ZEISS EVO 25

By Ivan Calandra

<!-- TOC ignore:true -->
# Table of content

<!-- TOC -->

- [Introduction](#introduction)
- [What and how to report](#what-and-how-to-report)
    - [Method section of a paper](#method-section-of-a-paper)
        - [SEM documentation](#sem-documentation)
        - [EDS measurements](#eds-measurements)
        - [Correlative microscopy](#correlative-microscopy)
        - [Commons](#commons)
    - [Data & Metadata](#data--metadata)
        - [General](#general)
        - [SEM images](#sem-images)
        - [EDS data](#eds-data)
        - [Correlative microscopy](#correlative-microscopy)

<!-- /TOC -->



# Introduction

This template explain what I think is important to report and how to report this information for scanning electron microscope (SEM) images acquired with the ZEISS EVO 25.  
The template is meant as an **easy and quick way to report extensive information (metadata) about microscope images**.

This template is split into two parts:

1. What to report in the method section of a paper
2. How to report all necessary metadata together with the data

In the first part, I provide a "fill-in-the-blanks" text that can be pasted into the method section of a paper. In the second, I will show that extensive metadata can be reported and shared without any effort, when the data are shared in appropriate formats.

While this template is specifically targeted at images from the ZEISS SEM, I believe that it can be adapted quite easily for images acquired with other SEMs.

This template is available as a markdown file (this file) as well as a [DOCX file](/Guidelines/ZEISS_EVO25.docx).

  
<br> 

# What and how to report

## Method section of a paper
I suggest to use the following text snippets. Parts in square brackets must be adjusted using the text within the brackets as examples or list to choose from. The rest of the text should of course also be adapted to the study.  
Settings and their values can alternatively be presented as tables, either in the main text (recommended) or as supplementary material. The report(s), or parts of it (them), from the Shiny App [imaging-reports](https://github.com/ivan-paleo/imaging-reports) can be used for this.  
See [https://doi.org/10.1016/j.jasrep.2024.104572](https://doi.org/10.1016/j.jasrep.2024.104572) for an example. 

### SEM documentation
"[*Objects*] were documented by SEM (Zeiss EVO 25) at the IMPALA, using the secondary electron detector ([*VPSE G4* or *SE1*]) at [*low* or *high*] vacuum ([*30*] Pa) and acceleration voltage of [*10*] kV. The objects were [*uncoated* or *coated with...*]."

### EDS measurements
"The elemental composition was measured by coupling the SEM (Zeiss EVO 25) equipped with a back-scattered electron detector (HDBSD) to an energy-dispersive X-ray spectrometer (EDX, Bruker Quantax XFlash 6|30 M). SEM and EDX were performed at [*low* or *high*] vacuum ([*~0.01*] Pa) and acceleration voltage [*20*] kV. The objects were [*uncoated* or *coated with...*]."

### Correlative microscopy
"The coordinate system was calibrated with the [objective(s) manufacturer and name(s) including nominal magnification(s) and numerical aperture(s)] objective on the [*digital microscope* and/or *light/confocal microscope*], and at 150x magnification on the scanning electron microscope."

### Commons
"All data in original formats, together with their metadata (acquisition and analysis settings), can be found on Zenodo ([*DOI*])."


<br>


## Data & Metadata
### General
The data should be uploaded on an open repository (e.g. Zenodo) in original formats to preserve the metadata as well as in open formats for reusability. Add a README file to the upload.  

Follow the instructions in the how-to's to [upload to Zenodo](/How-to/Zenodo.md) and to [read CZI or TIFF files with ImageJ2/Fiji](/How-to/ImageJ2-Fiji.md).

Even though many settings are included in the files as metadata, some of these settings should also be listed in the main text (see [Method section of a paper](#method-section-of-a-paper)).  

See [https://doi.org/10.5281/zenodo.10074758](https://doi.org/10.5281/zenodo.10074758) for an example.

### SEM images
- Upload the full-resolution, uncompressed and unedited SEM images in TIF format.
- Also upload the overview images (*_registration.png) showing the location of images on the object (red rectangle).
- Specify in the README: "SEM images were acquired with the software SmartSEM v. [6.08] from Zeiss ([https://www.zeiss.com/microscopy/en/products/software/zeiss-smartsem.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-smartsem.html)). All metadata (acquisition settings) are included in the TIF-files and can be retrieved using e.g. the IMBalENce plugin for ImageJ/Fiji ([https://imagej.net/plugins/imbalence](https://imagej.net/plugins/imbalence))."

### EDS data
- Upload files in original Bruker formats (SPX, PRF, RTO, RTL or BCF).
- Export spectra data to XLSX and upload them.
- Upload BSD images, showing the location of EDS spectra for each measurement point in case of measurements in the Objects workspace, in PNG format. These should be the same images as the BSD images from the SEM but at lower resolution and with less metadata.
- Specify in the README:
  - "EDX data were acquired and processed with the software Esprit v. [2.3.0.997] from Bruker ([https://www.bruker.com/en/products-and-solutions/elemental-analyzers/eds-wds-ebsd-SEM-Micro-XRF/software-esprit-family.html](https://www.bruker.com/en/products-and-solutions/elemental-analyzers/eds-wds-ebsd-SEM-Micro-XRF/software-esprit-family.html))."
  - "The individual spectra were exported to XLSX format for compatibility. The amount of metadata is limited."
  - Explain what each data type is.
  - Detail the quantification method (alternatively in the method).

### Correlative microscopy
- Upload ZEN Connect project(s) (project-name.a5proj).
- Upload images as CZI (all microscopes, see [Widefield images](/Guidelines/ZEISS_Optical-microscopes.md#widefield-images)) and/or TIF (SEM only, see [SEM images](#sem-images)), ideally in the ZEN connect data folder (project-name_data).
- Optionally, upload the image export(s) as PNG.
- Specify in the README: "ZEN Connect projects were created with Zeiss' ZEN desk v. [*3.5*] (blue edition, [https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-desk.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-desk.html)) software with the module ZEN Connect ([https://www.zeiss.com/microscopy/en/products/software/zeiss-zen/zen-connect-toolkit.html](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen/zen-connect-toolkit.html))."
