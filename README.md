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
    - [Digital zoom](#digital-zoom)
    - [Optical vertical resolution and depth of field](#optical-vertical-resolution-and-depth-of-field)
    - [Digital vertical resolution](#digital-vertical-resolution)
- [Processing](#processing)
- [Saving](#saving)
    - [Raw vs. derived data](#raw-vs-derived-data)
    - [File formats and software](#file-formats-and-software)
- [Reporting](#reporting)
- [Sharing](#sharing)
- [How to contribute](#how-to-contribute)
    - [Submit an issue](#submit-an-issue)
    - [Propose changes](#propose-changes)
    - [Send me an email](#send-me-an-email)
    - [Code of conduct](#code-of-conduct)
- [License](#license)
- [References](#references)

<!-- /TOC -->


---


## Introduction
This good-practice document is directed at archaeologists and paleontologists working with microscopes, but anyone working with microscope images might learn a few things here.  

Microscopes now deliver digital images. However, digital images are different to analog images and to what the observer/analyst sees through the oculars. Therefore, digital images have specific properties that must be reported in publications, so that other researchers have the necessary details to assess the published images and also so that they can repeat/reproduce these images.  

This document is by no means exhaustive and is limited in scope on purpose, but I hope it will help many archaeologists and paleontologists. 

As a disclaimer, **this document only presents my opinion**, at least for now. You are free to disagree. Whether you agree or not, I would really appreciate if you could share your opinion and [contribute](#how-to-contribute) to the development of this document so that it can be accepted by a larger community.


---


## Scale of observation
A microscope is obviously used to observe features of an object that are too small to be visible to the naked eye. To do so, a series of lenses magnifies the object so that the analyst sees more details. But which scale(s) is (are) appropriate and how to reach this (these) scale(s) with a microscope?

So, the first question the analyst should ask is: **What is the size of the features of interest?** It is important to consider the range of sizes: the size of the smallest features is important, but so is the size of the largest. This is because the larger this range, the less likely it is that all these sizes can be observed with a single set of settings. In other words, if features of different sizes are of interest, several acquisitions at different scales will probably be needed.  
Finding the size(s) of the features is often done directly during observation: increasing the magnification until the features of interest are visible. This is a valid approach if the microscope used has the appropriate hardware (objectives and optical zoom) to resolve the features of interest. But it can also happen that the features of interest are smaller or larger than what is permitted by the hardware at hand. Moreover, when dealing with digital images, some other issues might occur. This is why it is always advisable to start with at least a rough idea of the size(s) of the features and of the capabilities of the microscope(s) available to the analyst.  

But how do we know what the microscope's hardware can achieve in terms of scale? Most publications and reports talk about *magnification*. But what is it really and what does it mean? In the next section, I will argue that magnification is (almost) useless in digital microscope imaging and actually only confuses the analyst. Resolution is much more important, but it is unfortunately still cryptic to many analysts; I will therefore try to explain some concepts afterwards.


---


## Magnification 
Magnification is simply: the size of the magnified area divided by the real size of the imaged sample's area. This simple definition has wide-ranging implications in digital imaging. 


### Optical magnification
But let us first have a look at the optical magnification.  
The optical magnification of a microscope image when observed through the oculars is straightforward to calculate:   

$optical \ mag. = objective \ magnification \times ocular \ magnification \times optical \ zoom$ (1)

For example, using a 20x objective with 10x oculars and 2x optical zoom, the total optical magnification is 400x.


### Digital magnification
Things get more complicated in the digital world. It all comes down to one single question: **what is THE size of the magnified area when stored on a digital image?** Is it the size of the screen when you acquire the image? Is it the size of the screen when you view the image? Is it the size printed on paper, or projected to a screen? There is no single size for a digital image because it depends on the viewing medium: increase the size of the viewing medium and the magnification will increase as well, even though the image is the same. Does that mean that increasing the size of the viewing medium will improve the resolution? Unfortunately, no.  

Let us see how the digital magnification is calculated. The problem with a digital image (as opposed to an analog image) is that many components come into play to magnify the sample: both the optical (objective, optical zoom and camera adaptor) and digital (camera sensor, viewing medium and digital zoom) components must be considered. Note that the oculars are not relevant anymore because the light goes to the camera without passing through the oculars.  
This is how to calculate the digital magnification:  

$digital \ mag. = \frac{objective \ magnification \times optical \ zoom \times camera \ adaptor \times viewing \ medium \ diagonal \times digital \ zoom}{camera \ sensor \ diagonal}$  (2)

For example, using a 20x objective, 2x optical zoom, 1x camera adaptor, 381 mm or 15" screen diagonal (to be precise, what matters is the diagonal of the part of the screen where the image is displayed), 1x digital zoom, and 11 mm camera sensor diagonal, the total on-screen magnification is:  

$\frac{20 \times 2 \times 1 \times 381 \times 1}{11} \approx 1385 \times$ 

As you can see, with the same optical components (except oculars) as in the example calculation of the optical magnification above (see formula (1)), the resulting digital magnification is about 3.5 $\times$ larger than the optical magnification. **So digital and optical magnifications *are* different!**  

An example I like to show is the figure 8a of [Pedergnana (2020)](#references) (the paper can be read [here](https://rdcu.be/cWpDH)). According to the legend, the original magnification of the optical light microscopy image on the left is 10x and that of the SEM image on the right is 200x (actually 260x according to the data zone on the image itself). So different magnifications but same field of view and roughly same size on the PDF...?! Here I do not mean that Antonella Pedergnana was wrong; she actually did correctly report the microscopes' settings, which are misleading for the reader. This example shows that the concept of digital magnification is troublesome!

Also, the formula (2) shows that calculating the total digital magnification is not so easy in practice: the camera sensor diagonal and the viewing medium diagonal are not always known. 


### Banning magnification?
So what now? **Should we all forget about magnification in digital microscopy?** Well, pretty much, in my opinion.  

If the analyst has observed and analyzed while looking through the ocular, the optical magnification is very relevant and should be reported. However, the image published is a digital one. This implies that the analyst and the readers/audience will observe the sample at different magnifications (and resolutions as well, see the next section). In some cases, the readers/audience might not be able to see what the analyst is referring to. This might result in misunderstanding and potentially even disbelief in respect to the analyst. Even when the analyst analyzed the digital image directly, the viewing medium diagonal might change for each person anyway (laptop screen vs. desktop screen vs. projected screen...).  

As a side note, the field of view of a digital image is usually smaller (to avoid [vignetting](https://en.wikipedia.org/wiki/Vignetting)) than the field of view of the image as seen through the oculars. This is another source of differences when the analyst observed through the ocular but reports/publishes a digital image.

There is another reason for avoiding the digital magnification. When I was tasked to compare different digital microscopes (*i.e.* microscopes without oculars and where the image is directly and only viewed on a screen), I noticed that there were very large variations in the magnification ranges advertised by the different manufacturers. Looking at the small print, I realized that, for example, one manufacturer reported the magnification as seen on a 15" screen diagonal, while another one as seen on a 17.5" screen diagonal. This made sense because this was the size of the image as seen in the respective acquisition software packages. But this is very confusing to the buyer/user.  
Just for the comparison, let us simply change the screen from 15" to 17.5" (444.5 mm) in the example above:

$\frac{20 \times 2 \times 1 \times 444.5 \times 1}{11} \approx 1616 \times$

So this makes a significant difference!

There might be one case where the digital magnification might be useful, namely in SEM imaging. In this case, the digital magnification is given relative to a *reference*. For example, in the case of our Zeiss EVO 25, the magnification is given relative to the Polaroid 545 format (other formats can be selected), *i.e.* as if printed on 4 $\times$ 5" polaroid paper. This used to be the printing format for analog images in the days before digital SEMs. Note that other manufacturers might use different references so the magnifications might not be comparable, once again.


### Scale bar
So, if the digital magnification is useless, how can we know the size of a digital microscope image? The good old **scale bar**! The field of view, *i.e* the size of the imaged area of the sample, or rulers or anything similar will do the trick too.

**In summary, in my opinion, talking about *resolution* is much more useful and relevant than magnification.**


---


## Resolution
There is not one single resolution but many different, complementary definitions of resolution. First, it is important, once again, to differentiate between optical and digital resolutions. And second, there are lateral (XY) and vertical (Z) resolutions. 

The optical resolution is influenced by the optics (objective + optical zoom), while the digital resolution is influenced by the field of view (itself dependent on the objective) and the camera/detector.

Most terms and definitions here refer to the [Fair Data Sheet Initiative, v1.2α](http://www.optassyst.de/fairesdatenblatt/) (the website is only in German, but the Fair Data Sheet itself has an English version). I will abbreviate it "FDS".


### Optical lateral resolution
Due to aberrations from the optics and diffraction of the light, an optical system will be limited in its ability to distinguish points; the image will become blurry at the smallest scales. These effects are the basis for the calculation of the optical lateral resolution as defined by the [Rayleigh criterion](https://en.wikipedia.org/wiki/Angular_resolution).

The calculated optical lateral resolution is the "minimum theoretical distance between two adjacent, barely distinguishable features of an object" (FDS §2.2.8). In other words, if two points are closer from each other than the optical lateral resolution, then it is not possible to distinguish them (*i.e.* they will looks like one point only). They will appear as two separate points only if they are further from each other than the optical lateral resolution.

The calculated optical lateral resolution $\delta_L$ depends on the numerical aperture of the optics (= objective + optical zoom, $NA$), on the wavelength of the light $\lambda$ and on a factor $K$:

$\delta_L = \frac{K.\lambda}{NA}$ (3)

The value of $K$ is 0.61 for bright field microscopy (= "classical" light microscopes). For laser-scanning confocal microscopy, $K$ depends on the diameter of the pinhole and varies between 0.37 and 0.61 ([Artigas 2011](#references)).

From formula (3) and the definition of the optical lateral resolution, it becomes apparent that **the smaller $\delta_L$, the better the resolving power of the microscope** (*i.e.* closer points will be distinguishable). This is what we usually refer to as "*higher* resolution", even though the value for $\delta_L$ is *smaller*. Confusing, right? This is why I prefer to talk about "better/worse" resolution rather than "smaller/larger".

The NOTE 3 of the FDS §2.2.8 states that "the optical [lateral] resolution can be achieved only under ideal conditions (including complete illumination of the pupil) on planar objects. This value is usually not reached on textured surfaces". In archaeology and paleontology, we usually deal with textured surfaces!


### Digital lateral resolution
The digital lateral resolution, or *measuring point spacing*, is the "sampling interval of measuring points in the measuring volume, both in X and in Y direction" (FDS §2.2.7). This is also referred to as the *pixel size* (pixel size can also refer to the size of the photodiodes on the detector/camera, which is a fixed value independent of the field of view) or *spatial sampling*.

The measuring point spacing is calculated by dividing the *measuring area* (FDS §2.2.1, also called *field of view*) by the *maximum number of measuring points in a single measurement* (FDS §2.1.2, also called *frame size* or *number of pixels*):

$measuring \ point \ spacing = \frac{measuring \ area}{number \ of \ pixels}$ (4)


### Relationship between optical and digital lateral resolutions
So far, so good, and not too complicated. The problem is that we now have two different values for the lateral resolution. Which one should we care about? Both, of course! But **what should the relationship between optical and digital lateral resolutions be?** 

The Nyquist criterion (based on [Nyquist–Shannon sampling theorem](https://en.wikipedia.org/wiki/Nyquist%E2%80%93Shannon_sampling_theorem)) states that [the digital lateral resolution should be 2-3 times smaller than the optical lateral resolution](https://zeiss-campus.magnet.fsu.edu/articles/basics/digitalimaging.html). This is necessary to digitally image with sufficient details the transition between features that are optically visible.  
For example, if $\delta_L = 0.6 \ \mu m$, then the measuring point spacing should be 0.2-0.3 µm.  

If the digital lateral resolution is more than 3 times smaller than the optical lateral resolution, this will result in oversampling: adjacent pixels will have the same values, so the digital image will not contain more meaningful information but simply more information. This results in larger files than necessary and generally does not improve the quality of the image.  
If the digital lateral resolution is less than 2 times smaller than the optical lateral resolution, this will result in undersampling: the transition between features that are optically visible will not be visible on the digital image.


### Digital zoom
Formula (2) includes the digital zoom in the calculation of the digital magnification, but it is not part of formula (4) for the digital lateral resolutions. So what happens when zooming in *digitally*?

Let us start with an original image 100 $\times$ 100 µm  with 1000 $\times$ 1000 pixels. This results in a measuring point spacing of 0.1 µm.  
The digital zoom acts like a cropping and enlarging tool: the original image will be first cropped and then enlarged to the same viewing size as the original image.  
A digital zoom factor 2x means that the original image is cropped by half in X and in Y directions, *i.e.* the zoomed image is 4  $\times$ smaller than the original image. This is true both for the size in µm and for the number of pixels. The zoomed image will therefore be 50 $\times$ 50 µm but it will occupy the same space on your screen as the original image (*i.e.* digital magnification 2 $\times$ larger). And it will have 500 $\times$ 500 pixels.  
So what about the digital lateral resolution of the zoomed image? 0.1 µm, just like the original image.

All this to say that the **digital zoom obviously changes the digital magnification but does not influence the digital lateral resolution**.  

Still, it seems that zooming in digitally helps to see more details. This is just because the details are displayed larger on the screen, not because they are better resolved. For a better digital resolution, a smaller field-of-view for the same number of pixels, or more pixels for the same field-of-view, is needed. This can be achieved by using a higher magnification objective and/or an optical zoom, or a camera with more pixels.


### Optical vertical resolution and depth of field
The optical vertical, or axial, resolution is equal to the depth of field for a bright field (BF) microscope:

$\delta_A(BF) = depth \ of \ field = \frac{n.\lambda}{NA^2}$ (5)

with $n$ the refractive index of the medium; $n_{air} \approx 1$. 

For a confocal microscope, the axial resolution is calculated by the optical slice thickness, which also depends on the pinhole diameter ([Artigas 2011](#references)):

$\delta_A(conf) = \frac{0.64 \lambda}{n- \sqrt{n^2-NA^2}}$ (6) with a pinhole diameter $PH < 0.25 AU$ ([Airy Unit](https://en.wikipedia.org/wiki/Airy_disk))

$\delta_A(conf) = \sqrt{(\frac{0.88 \lambda}{n- \sqrt{n^2-NA^2}})^2 + (\frac{n.PH.\sqrt{2}}{NA})^2}$ (7) with a pinhole diameter $PH$ $\ge 0.25 AU$

Here again, **the smaller $\delta_A$, the better the resolution is.**


### Digital vertical resolution
The digital vertical resolution is meaningless in case of a 2D image (even for extended depth of focus - EDF - images) but it is relevant for 2.5 and 3D images. Unfortunately, I do not know how to calculate the digital vertical resolution of a z-stack.  
If anyone knows more about it, please [contribute](#how-to-contribute)!


---


## Processing
Few images are published without some form of processing. Sometimes, processing is even necessary to create (e.g. EDF, stitching, topography reconstruction) or analyze (e.g. contrast/brightness, surface texture analysis) the image.  
While processing deserves a whole good-practice document on its own, I would just like to give some general advices here that will hopefully be applicable to most processing routines. But feel free to [contribute](#how-to-contribute)!

Even if we sometimes tend to assume that there is only one way to process an image, there are in fact often several methods or algorithms to do so, and there are always various settings to adjust. This is why it is important to **be as precise as possible when reporting about the processing** (see section [Reporting](#reporting)).  

It is also crucial to **process all images of a dataset in the same way**. This might seem obvious, but different processing methods might produce results that might appear identical/similar even if they actually are different. Processing all images in the same way ensures that all images are comparable at least within a dataset. Of course, this is true only if **the images were acquired in the same way**!  
So, while the details are more nuanced, I believe the message is clear and every analyst should try his/her/their best to acquire and process images and data in a consistent and comparable manner.

Another general piece of advice is to **keep the raw data**, in this case the acquired image, and to **process a copy** of it rather than overwriting the acquired image. This way, it is possible to check the result and process differently if necessary. See section [Saving](#saving) for a discussion on raw/derived data and file formats.

Last but not least, it is important to **keep a very detailed record of the processing and analysis steps that were performed**. Templates and scripts will make it easier to repeat and reproduce the processing/analysis. This is not only important to share data (see section [Sharing](#sharing)); it is also important for yourself as it is likely that you will have to repeat the analysis at some point, at least for some images.


---


## Saving

### Raw vs. derived data
I totally agree with Ben Marwick and colleagues that raw data should be kept raw and clearly separated from derived data (e.g. [Marwick et al. 2018, Marwick & Pilaar Birch 2018](#references)).  

Still, it is not always clear to distiguish between the two, nor practicable to keep the raw(est) data. For example, the raw data of an EDF image or a 2.5D topographical model (= height map, e.g. from a confocal microscope) is a z-stack. The z-stacks can be very large files so keeping all these z-stacks requires a lot of storage space. While storage is not really limiting anymore, the environmental impacts of data centers and online repositories cannot be ignored (e.g. [Samuel & Lucivero 2020](#references)).  

Also the derived data of an analysis can be the raw data of another. Using the example of surface texture analysis (dental microwear texture analysis or quantitative artifact microwear analysis), the raw data of the analysis are the height maps (which are themselves derived from processing the z-stacks) that are used as input for MountainsMap (or equivalent) to calculate the surface texture parameters for each height map, which are eventually exported into a CSV file. This CSV file is in-turn the raw data for the subsequent statistical analysis.  

All this to say that the decision should be made on a case-by-case basis about what data is raw and what is derived. Nevertheless, there are some general principles that apply in most (all?) cases, make sure to:

- **save the rawest data possible**, usually the acquired, unprocessed image;
- **save every derived data that is included in the final analyis** (i.e. input data of the results), especially if the processing/analyes are not fully automatized;
- **save all the metadata** associated with the raw data (see section [File formats and software](#file-formats-and-software));
- **save in appropriate format(s)** (see section [File formats and software](#file-formats-and-software)).

### File formats and software
For long-term usability, accessibility and sustainability, proprietary formats (i.e. files that can only be opened with a paid software) should be avoided and **stable, open, non-proprietary formats should be preferred**. The DANS maintains a [list of preferred and non-preferred formats](https://dans.knaw.nl/en/file-formats/). For microscopy images, the [OME-TIFF format](https://docs.openmicroscopy.org/ome-model/6.3.1/ome-tiff/index.html) is probably the standard.  
Most microscope manufacturers offer software packages to acquire images; in some cases, these software packages are even necessary to operate the microscopes. Not all of these software packages can save in an open format, even less so in OME-TIFF. Unfortunately, metadata sometimes get lost when the image is not saved in the native, proprietary format.  
This is why, if your acquisition software cannot natively save in an open format, ***I* would recommend to save the image in the proprietary format** (in order to save all the metadata) **and to additionally export to an open format** (for long-term accessibility).

Following on this discussion, it is therefore important to favor open-source software packages over paid ones. Nevertheless, open-source projects often have difficulties to keep running and being developed (see e.g. [Coelho & Valente 2017](#references)). Also, open-source software packages are often less user-friendly, and are slower to add new functionalities and to adapt to OS upgrades. So, open-source is not always better.  
Still, [Fiji and ImageJ](https://imagej.net/) is a great open-source solution for image analysis with a 25-year-long history (meaning it is likely to survive). [Bio-Formats](https://www.openmicroscopy.org/bio-formats/) is an important "software tool for reading and writing image data using standardized, open formats", which is incorporated into ImageJ. Some microscope manufacturers also offer a free viewer or a free light version (e.g. Zeiss' [ZEN starter](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-starter.html) and [ZEN lite](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-lite.html)).


---


## Reporting
All the background information of the previous sections aims at providing the required knowledge to use a microscope to reach the desired scale of observation and to save all the acquired data and metadata. While it is important for the analyst to see what he/she/they want to see on the sample, it is equally important that the reader/audience that will be presented - or even will assess - the work is able to know what can be observed in terms of scale on the reported/published/shared images. This is also important for *repeatability* and *reproducibilty* (and *pre-producibility* *sensu* [Stark 2018](#references)).  

The importance of reporting for microscopy is not unique to archaeology/paleontology (see e.g. [Calandra et al. 2019](#references)) and other fields also suffer from a lack of high-quality reporting (see e.g. [Marqués et al. 2020](#references) in biomedical research).

So here is a list of what I think is necessary for pre-producible microscope images. This list should be adapted according to the equipment/software used.


**Number**|**Category**|**What?**|**Why?**|**How? (examples)**  
-----|-----|-----|-----|-----  
1|Observation/analysis method|Observation/analysis through oculars or directly on the digital image? |To know how the analyst performed the analysis|“The features were observed and analyzed through the oculars. The images reported are therefore not equivalent to what has been observed during analysis.”  
2|Microscope|Manufacturer and model of the microscope  |To account for all (unknown) settings that are part of the microscope’s design|“AxioScope.A1 (Carl Zeiss Microscopy GmbH)”  
3|Technique|Imaging technique / contrast|To interpret the image according to the technique(s) used|“Confocal microscopy” or “bright field” or “DIC”  
4|Light|Illumination|To interpret the image according to the illumination(s) used|“Ringlight illumination” or “Coaxial illumination”  
5|Light|Type + wavelength of the light source  |To calculate the optical resolutions|“Violet LED 405 nm”  
6|Light|Light source intensity|To be able to repeat the acquisition|"60%"
7|Light|Exposure time|To be able to repeat the acquisition|"100 ms"
8|Optics|Objective specifications|To calculate magnifications and resolutions|“Objective Zeiss C Epiplan-Apochromat Mag. = 50 $\times$ / NA = 0.95 / WD = 0.22 mm”  
9|Optics|Oculars magnification, if applicable (see #1)|To calculate the optical magnification|“10 $\times$ oculars”
10|Optics|Optical zoom, if applicable  |To calculate magnifications|“2 $\times$ optical zoom”
11|Camera|Digital zoom, if applicable  |To calculate the digital magnification|“2 $\times$ digital zoom”
12|Camera|Measuring point spacing + field of view + number of pixels (at least two of them)  |To calculate the digital lateral resolution|“100 $\times$ 100 µm for 1000 $\times$ 1000 pixels” or “1000 $\times$ 1000 pixels, measuring point spacing = 0.1 µm”
13|Camera|Scale bar  |To visualize the size of the imaged region|“Scale bar = 100 µm”
14|Confocal|Pinhole diameter, if applicable  |To calculate the optical resolutions|“PH = 54 µm (1 AU)”
15|Confocal|Step size + z-range, if applicable|To be able to repeat the measurement|“40-50 µm with 0.2 µm steps”
16|Confocal|Temperature + humidity during topography scanning|T & H can influence the fine-scale measurements of topography|“Scans were acquired at 20 < T < 22 °C and 50 < rH < 70 %”
17|Confocal|Location of the equipment|An environment without vibrations is necessary for fine-scale measurements of topography|“The confocal microscope is located in the basement and placed on a passive anti-vibration table, itself placed on a concrete based decoupled from the rest of the floor”
18|Confocal|Any other equipment-specific setting|To be able to repeat the measurement|"Master gain = 220 V"
19|Software|Versions of acquisition and analysis software packages|Different versions might produce different results|“ZEN blue 3.5 Hotfix 7 (Carl Zeiss Microscopy GmbH) with module Shuttle-and-Find” or “ConfoMap 9.2.10042 with module Scale-sensitive Analysis”
20|Processing|Stitching, if applicable|To be able to repeat the processing|"2 $\times$ 2 tile regions were acquired, with shading correction (to avoid seeing the separations between single images), 5% minimal overlap and 10% maximal shift, 'optimized' comparer and 'best' global optimizer.  
21|Processing|Extended depth of focus (EDF), if applicable|To be able to repeat the processing|"Z-stacks were processed to EDF images with the wavelets method and without z-stack alignment"
22|Processing|Image enhancements / filters / image analysis settings, if applicable|To be able to repeat the processing|"The contour were enhanced with settings A and B; and brightness, contrast and gamma were adjusted to C, D and E respectively"
23|Processing|Workflow and settings of the surface texture analysis, if applicable|To be able to repeat the processing|"The surface texture analysis was performed with the following template [add analysis details and link to template]"

From my point of view, **all of these pieces of information should be published together with every microscope acquisition**.


---


## Sharing
A lot could be said about data sharing and Open Science. I will keep it brief here and focused on microscope images; more general aqnd extensive discussions can be found in e.g. [Marwick & Pilaar Birch 2018, Gomes et al. 2022, Karoune & Plomp 2022](#references).

**In my opinion, publishing only a few, supposedly representative images of the whole dataset is not enough** because of the following reasons:
1. The sample might be representative in some aspects but not in others. 
2. To be honest, in most cases, only the "nicest" images are published and the least informative/relevant are not; this implies a strong bias and the true signal might just be lost by this selective sampling/reporting. 
3. Images published in a journal article are usually small and of reduced quality, so the published images might not even show what can be seen on the full-scale image.
4. Without seeing all images in full resolution, how can anyone assess whether the data support the conclusions? 
5. It would be a shame to keep all these images for yourself.
6. Why should we show only a small part of the extensive work we did? Let us do ourselves a favor and show how hard we work! 

**In addition to detailed reporting** (see section [Reporting](#reporting)), **I would therefore recommend:**
1. **to keep showing a sample as representative as possible in the journal article, but**
2. **to additionally upload all images with their metadata to an online repository** .

I would like to stress that the data should be uploaded to a trustworthy online repository (e.g. [Zenodo](https://zenodo.org/), [OSF](https://osf.io/), [Figshare](https://figshare.com/)) rather than as online supplementary information (SI) to the article. This is because SI might be behind a paywall, just like the article. Even when it is not, publishers might have restrictions about file formats and names. And since everyone does mistakes, it is easier to correct them if you have access to the repository rather than relying on the publisher to do it (which can take a long time or might even never happen).  
Here again, the discussion about raw/derived data and file formats is important (see section [Saving](#saving)).  


---


## How to contribute
I appreciate any comment from anyone (expert or novice) to improve this document, so do not be shy! There are three possibilities to contribute:

### Submit an issue  
If you notice any problem or have a question, submit an [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues). You can do so [here](https://github.com/ivan-paleo/publish-micro-image/issues).  
A GitHub account is necessary. 

### Propose changes  
This document is written in [Markdown](https://www.markdownguide.org/). If you know how to write in this format, please propose text edits as a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) (abbreviated "PR").  
A GitHub account is necessary. 

### Send me an email  
If you do not have a GitHub account and do not want to sign up, you can still write me an email (Google my name together with my affiliation to find my email address).

### Code of conduct
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
Artigas R. 2011. Imaging Confocal Microscopy. In: Leach R ed. Optical Measurement of Surface Topography. Berlin, Heidelberg: Springer Berlin Heidelberg, 237–286. https://doi.org/10.1007/978-3-642-12012-1_11

Calandra I, Schunk L, Bob K, Gneisinger W, Pedergnana A, Paixao E, Hildebrandt A, Marreiros J. 2019. The effect of numerical aperture on quantitative use-wear studies and its implication on reproducibility. Scientific Reports 9: 6313. https://doi.org/10.1038/s41598-019-42713-w

Coelho J, Valente MT. 2017. Why modern open source projects fail. In: Proceedings of the 2017 11th Joint Meeting on Foundations of Software Engineering and the ACM SIGSOFT Symposium on the Foundations of Software Engineering, Paderborn, Germany. 186–196. https://doi.org/10.1145/3106237.3106246

Gomes DGE, Pottier P, Crystal-Ornelas R, Hudgins EJ, Foroughirad V, Sánchez-Reyes LL, Turba R, Martinez PA, Moreau D, Bertram MG, Smout CA, Gaynor KM. 2022. Why don’t we share data and code? Perceived barriers and benefits to public archiving practices. Proceedings of the Royal Society B: Biological Sciences 289: 20221113. https://doi.org/10.1098/rspb.2022.1113

Karoune E, Plomp E. 2022. Removing Barriers to Reproducible Research in Archaeology. Zenodo, ver. 5 peer-reviewed and recommended by Peer Community in Archaeology. https://doi.org/10.5281/zenodo.7320029

Marqués G, Pengo T, Sanders MA. 2020. Imaging methods are vastly underreported in biomedical research. eLife 9: e55133. https://doi.org/10.7554/eLife.55133

Marwick B, Pilaar Birch SE. 2018. A Standard for the Scholarly Citation of Archaeological Data as an Incentive to Data Sharing. Advances in Archaeological Practice 6: 125–143. https://doi.org/10.1017/aap.2018.3

Marwick B, Boettiger C, Mullen L. 2018. Packaging Data Analytical Work Reproducibly Using R (and Friends). The American Statistician 72: 80–88. https://doi.org/10.1080/00031305.2017.1375986

Pedergnana A. 2020. “*All that glitters is not gold*”: Evaluating the Nature of the Relationship Between Archeological Residues and Stone Tool Function. Journal of Paleolithic Archaeology 3: 225–254. https://doi.org/10.1007/s41982-019-00039-z

Samuel G, Lucivero F. 2020. Responsible Open Science: Moving towards an Ethics of Environmental Sustainability. Publications 8: 54. https://doi.org/10.3390/publications8040054

Soler S. 2022.cc-licenses: Creative Commons Licenses for GitHub Projects. Available at https://github.com/santisoler/cc-licenses (accessed September 27, 2022)

Stark PB. 2018. Before reproducibility must come preproducibility. Nature 557: 613–613. https://doi.org/10.1038/d41586-018-05256-0