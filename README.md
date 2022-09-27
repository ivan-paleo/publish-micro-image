# publish-micro-image

**How to publish microscope images**



**Table of content**

<!-- TOC depthfrom:2 -->

- [Introduction](#introduction)
- [Scale of observation](#scale-of-observation)
- [Magnification](#magnification)
    - [Optical magnification](#optical-magnification)
    - [Digital magnification](#digital-magnification)
    - [Banning magnification?](#banning-magnification)
    - [Scale bar](#scale-bar)
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
But let us first have a look at the optical magnification.  
The optical magnification of a microscopic image when observed through the oculars is also straightforward to calculate:   

$objective \ magnification \times ocular \ magnification \times optical \ zoom$ (1)

For example, using a 20x objective with 10x oculars and 2x optical zoom, the total optical magnification will be 400x.


### 3.2. Digital magnification
Things get more complicated in the digital world. It all comes down to one single question: **what is THE size of the magnified area when stored on a digital image?** Is it the size of the screen when you acquire the image? Is it the size of the screen when you view the image? Is it the size printed on paper, or projected to a screen? There is no single size for a digital image because it depends on the viewing medium: increase the size of the viewing medium and the magnification will increase as well, even though the image is the same. Does that mean that increasing the size of the viewing medium will improve the resolution? Unfortunately, no.  

Let us see how the digital magnification is calculated. The problem with a digital image (as opposed to an analog image) is that many component come into play to magnify the sample: both the optical (objective, optical zoom and camera adaptor) and digital (camera sensor, viewing medium and digital zoom) components must be considered. Note that the oculars are not relevant anymore because the light goes to the camera without passing through the oculars. 
This is how to calculate the digital magnification:  

$\frac{objective~magnification \times optical~zoom \times camera~adaptor \times viewing~medium~diagonal \times digital~zoom}{camera~sensor~diagonal}$  (2)

For example, using a 20x objective, 2x optical zoom, 1x camera adaptor, 381 mm screen diagonal (= 15"), 1x digital zoom, and 11 mm camera sensor diagonal, the total on-screen magnification is:  

$\frac{20 \times 2 \times 1 \times 381 \times 1}{11} \approx 1385 \times $ 

As you can see, with the same optical components (except oculars) as in the example calculation of the optical magnification above (see formula (1)), the resulting digital magnification is about 3 $\times$ larger than the optical magnification. **So digital and optical magnifications *are* different!**  

An example I like to show is the figure 8a of Pedergnana (2020) (the paper can be read [here](https://rdcu.be/cWpDH)). According to the legend, the original magnification of the optical light microscopy image on the left is 10x and that of the SEM image on the right is 200x (actually 260x according to the data zone on the image itself). So different magnifications but same field-of-view and roughly same size on the PDF...?! Here I do not mean that Antonella Pedergnana was wrong, but rather that the concept of digital magnification is useless!

Also, the formula (2) shows that calculating the total digital magnification is not so easy in practice: the camera sensor diagonal and the viewing medium diagonal are not always known. 


### 3.3. Banning magnification?
So what now? **Should we all forget about magnification in digital microscopy?** Well, pretty much, in my opinion.  

If the analyst has observed and analyzed while looking through the ocular, the optical magnification is very relevant. However, the image reported and published is a digital one. This implies that the analyst and the readers/audience will observe the sample at different magnifications (and resolutions as well, see the next section). In some cases, the readers/audience might not be able to see what the analyst is referring too. This might result in misunderstanding and potentially even disbelief in respect to the analyst. Even when the analyst analyzed the digital image directly, the viewing medium diagonal might change for each person anyway (laptop screen vs. desktop screen vs. projected screen...).  

As a side note, the field-of-view of a digital image is usually smaller (to avoid [vignetting](https://en.wikipedia.org/wiki/Vignetting)) than the field-of-view of the image as seen through the oculars. This is another source of differences when the analyst observed through the ocular but reports/publishes a digital image.

There is another reason for avoiding the digital magnification. When I was tasked to compare different digital microscopes (*i.e.* microscopes without oculars and where the image is directly and only viewed on a screen), I noticed that there were very large variations in the magnification ranges advertised by the different manufacturers. Looking at the small print, I realized that one manufacturer reported the magnification as seen on a 15" screen diagonal, while another one as seen on a 17.5" screen diagonal. This made sense because this was the size of the image as seen in the respective acquisition software packages. But this is very confusing to the buyer/user.  
Just for the comparison, let us simply change the screen from 15" to 17.5" (444.5 mm) in the example above:

$\frac{20 \times 2 \times 1 \times 444.5 \times 1}{11} \approx 1616 \times $

So this makes a significant difference!

There might be one case where the digital magnification might be useful, namely in SEM imaging. In this case, the digital magnification is given relative to a *reference*. For example, in the case of our Zeiss EVO 25, the magnification is given relative to the Polaroid 545 format (other formats can be selected), *i.e.* as if printed on 4 $\times$ 5" polaroid paper. This used to be the printing format for analog images in the days before digital SEMs. Note that other manufacturers might use difference references so the magnifications might not be comparable, once again.


### 3.4. Scale bar
So, if the digital magnification is useless, how can we know the size of a digital microscopic image? The good old **scale bar**! The field-of-view, *i.e* the size of the imaged area of the sample, or rulers or anything similar will do it too.

In my opinion, talking about *resolution* is much more useful and relevant than digital magnification.


---


## 4. Resolution
There is not one single resolution but many different, complementary definitions of resolution. First, it is important, once again, to separate optical and digital resolutions. And second, there are lateral (XY) and vertical (axial, Z) resolutions.  

Most terms and definitions here refer to the [Fair Data Sheet Initiative, v1.2α](http://www.optassyst.de/fairesdatenblatt/) (the website is only in German, but the Fair Data Sheet itself is in both German and English).

### 4.1. Optical lateral resolution

### 4.2. Digital lateral resolution

### 4.3. Relationship between optical and digital lateral resolutions

### 4.4. Optical vertical resolution and depth of field

### 4.5. Digital zoom


---


## 5. What should we report?


---


## 6. How to contribute
I appreciate any comment from anyone (expert or novice) to improve this document, so do not be shy! There are three possibilities to contribute:

### 6.1. Submit an issue  
If you notice any problem or have a question, submit an [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues). You can do so [here](https://github.com/ivan-paleo/publish-micro-image/issues).  

### 6.2. Propose changes  
This document is written in [Markdown](https://www.markdownguide.org/). If you know how to write in this format, please propose text edits as a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) (abbreviated "PR").

### 6.3. Send me an email  
For options 1-2, you need to create a GitHub account. If you do not have one and do not want to sign up, you can still write me an email (Google me to find my email address).

By participating in this project, you agree to abide by our [code of conduct](CONDUCT.md).


---


## 7. License
[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg


---


## 8. References
License badge and text from Santiago Soler's [cc-licenses](https://github.com/santisoler/cc-licenses).

Pedergnana, A. (2020). *"All that glitters is not gold"*: Evaluating the Nature of the Relationship Between Archeological Residues and Stone Tool Function. Journal of Paleolithic Archaeology 3: 225–254. https://doi.org/10.1007/s41982-019-00039-z