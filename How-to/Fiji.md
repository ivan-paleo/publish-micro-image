
<!-- TOC ignore:true -->
# How to open CZI files with Fiji

By Ivan Calandra

<!-- TOC ignore:true -->
# Table of content

<!-- TOC -->

- [Introduction](#introduction)
- [Download and install Fiji](#download-and-install-fiji)
- [Import CZI file](#import-czi-file)

<!-- /TOC -->



# Introduction

This document explains the main steps to open CZI files from Zeiss microscopes with Fiji/ImageJ and access their metadata. [CZI](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen/czi-image-file-format.html) is an open format, part of the [Bio-Formats](https://bio-formats.readthedocs.io/en/stable/formats/zeiss-czi.html).

ImageJ ([ImageJ2](https://imagej.net/software/imagej2/) for the most recent version) is an open-source software for scientific imaging. It is a very powertool to process scientific images, like microscope images.  
Fiji, which means ["Fiji Is Just ImageJ"](https://github.com/fiji/fiji), is ["an image processing package—a “batteries-included” distribution of ImageJ2, bundling a lot of plugins which facilitate scientific image analysis"](https://imagej.net/software/fiji/). One such plugin is [Bio-Formats](https://imagej.net/formats/bio-formats), which is necessary to open the CZI files.  

The steps presented below can be run with either ImageJ2 + plugin Bio-Formats, or directly with Fiji.


# Download and install Fiji
Download and install Fiji from the [official website](https://imagej.net/software/fiji/downloads) and follow the installation instructions there. 

There is actually no installation required. Unzip the downloaded file and move the extracted folder (`Fiji.app`) to a location where you have read and write access, for example in `C:\Users\[your name]\`.  

To open and run Fiji, simply open the file `ImageJ-win64.exe`.


# Import CZI file
In Fiji, go to `Plugins` > `Bio-Formats` > `Bio-Formats Importer` and select the file you want to open.
