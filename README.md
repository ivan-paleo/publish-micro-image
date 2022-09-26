# publish-micro-image

**How to publish microscope images**



**Table of content**

<!-- TOC depthfrom:2 -->

- [Introduction](#introduction)
- [Scale of observation](#scale-of-observation)
- [Magnification](#magnification)
    - [Optical magnification](#optical-magnification)
    - [Digital magnification](#digital-magnification)
    - [Scale bar](#scale-bar)
    - [Banning magnification?](#banning-magnification)
- [Resolution](#resolution)
    - [Optical lateral resolution](#optical-lateral-resolution)
    - [Digital lateral resolution](#digital-lateral-resolution)
    - [Relationship between optical and digital lateral resolutions](#relationship-between-optical-and-digital-lateral-resolutions)
    - [Optical vertical resolution and depth of field](#optical-vertical-resolution-and-depth-of-field)
    - [Digital zoom](#digital-zoom)
- [What should we report?](#what-should-we-report)
- [How to contribute](#how-to-contribute)
    - [Submit an issue](#submit-an-issue)
    - [Propose changes](#propose-changes)
    - [Send me an email](#send-me-an-email)
- [License](#license)
- [References](#references)

<!-- /TOC -->


---


## 1. Introduction
This good-practice document is directed at archaeologists and paleontologists working with microscopes, but anyone working with microscope images might learn a few things here.  
Microscopes now deliver digital images. However, digital images are different to analog images and to what the observer/analyst sees through the oculars. Therefore, digital images have specific properties that must be reported in publications, so that other researchers have the necessary details to assess the published images and also so that they can repeat/reproduce these images.  
This document is by no means exhaustive and is limited in scope on purpose. 


---


## 2. Scale of observation
A microscope is obviously used to observe features of an object that are not visible to the naked eye. To do so, a series of lenses magnifies the object so that the analyst sees more details. But which scale(s) is (are) appropriate and how to reach this (these) scale(s) with a microscope?

So, the first question the analyst should ask is: **What is the size of the features of interest?** It is important to consider the range of sizes: the size of the smallest features is important, but so is the size of the largest. This is because the larger this range, the less likely it is that all these sizes can be observed with a single set of settings. In other words, if features of different sizes are of interest, several acquisitions at different scales will probably be needed.  
Finding the size(s) of the features is often done directly during observation: increasing the magnification until the features of interest are visible. This is a valid approach is the microscope used has the appropriate hardware (objectives) to resolve the features of interest. But it can also happen that the features of interest are smaller or larger than what is permitted with the hardware at hand. Moreover, when dealing with digital images, some other issues might occur. This is why it is always advisable to start with at least a rough idea of the size(s) of the features and of the capabilities of the microscope(s) available to the analyst.  

It is now clear that it is important to know what the microscope's hardware can achieve in terms of scale. But how do we know that? Most publications and reports talk about *magnification*. But what is it really and what do it mean? In the next section, I will argue that magnification is (almost) useless in digital microscopic imaging and actually only confuses the analyst. Resolution is much more important, but it is unfortunately still cryptic to many analyst; I will therefore try to explain some concepts afterwards.


---


## 3. Magnification 
Magnification is simply: the size of the magnified area divided by the real size of the area. This simple definition has wide-ranging implications in digital imaging. 

### 3.1. Optical magnification
The optical magnification of a microscopic image when observed through the oculars is also straightforward to calculate: magnification of the objective, multiplied by the magnification of the oculars, multiplied by the optical zoom factor (if applicable).  
For example, using a 20x objective with 10\times oculars and 2x optical zoom, the total optical magnification will be 400x.

### 3.2. Digital magnification
Things get more complicated in the digital world. It all comes down to one single question: **what is THE size of the magnified area when stored on a digital image?** Is it the size of the screen when you acquire the image? Is it the size of the screen when you view the image? Is it the size printed on paper or projected to a screen? There is no single size for a digital image because it depends on the viewing medium: increase the size of the viewing medium and the magnification will increase as well, even though the image is the same. Does that mean that increasing the size of the viewing medium will improve the resolution? Unfortunately, no.  

Let us first have a look at how the digital magnification is calculated. The problem with a digital image (as opposed to an analog image) is that many component come into play to magnify the sample: both the optical (objective, optical zoom and camera adaptor) and digital (camera sensor, viewing medium and digital zoom) components must be considered.  
This is how to calculate the digital magnification:  
$\frac{objective magnification \times optical \,zoom \times camera \,adaptor \times viewing \,medium \,diagonal \times digital \,zoom}{camera \,sensor \,diagonal}$ 


### 3.3. Scale bar

### 3.4. Banning magnification?


---


## Resolution

### Optical lateral resolution

### Digital lateral resolution

### Relationship between optical and digital lateral resolutions

### Optical vertical resolution and depth of field

### Digital zoom


---


## What should we report?


---


## How to contribute
I appreciate any comment from anyone (expert or novice) to improve this document, so do not be shy! There are three possibilities to contribute:

### Submit an issue  
If you notice any problem or have a question, submit an [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues). You can do so [here](https://github.com/ivan-paleo/publish-micro-image/issues).  

### Propose changes  
This document is written in [Markdown](https://www.markdownguide.org/). If you know how to write in this format, please propose text edits as a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) (abbreviated "PR").

### Send me an email  
For options 1-2, you need to create a GitHub account. If you do not have one and do not want to sign up, you can still write me an email (Google me to find my email address).

By participating in this project, you agree to abide by our [code of conduct](CONDUCT.md).


---


## License
[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg


---


## References
License badge and text from Santiago Soler ([cc-licenses](https://github.com/santisoler/cc-licenses)).