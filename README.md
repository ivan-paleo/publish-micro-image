# publish-micro-image
Ivan Calandra
, 2025-04-09, 17:44:16

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
  - [Digital zoom](#digital-zoom)
  - [Optical vertical resolution and depth of
    field](#optical-vertical-resolution-and-depth-of-field)
  - [Digital vertical resolution](#digital-vertical-resolution)
  - [Relationship between optical and digital
    resolutions](#relationship-between-optical-and-digital-resolutions)
- [Scale, magnification, resolution -
  summary](#scale-magnification-resolution---summary)
- [Processing](#processing)
  - [Definitions](#definitions)
  - [Recommendations](#recommendations)
- [Saving](#saving)
  - [Raw vs. derived data](#raw-vs-derived-data)
  - [File formats and software](#file-formats-and-software)
  - [JPEG, PNG, TIFF, RAW](#jpeg-png-tiff-raw)
- [Reporting and sharing](#reporting-and-sharing)
  - [Minimum reporting requirements](#minimum-reporting-requirements)
  - [Sharing](#sharing)
  - [Instrument-specific guidelines](#instrument-specific-guidelines)
- [How to contribute](#how-to-contribute)
- [License](#license)
- [References](#references)

------------------------------------------------------------------------

**Recommendations on how to publish microscope images**

*The releases are available and citable on Zenodo*  
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.7503328.svg)](https://doi.org/10.5281/zenodo.7503328)

------------------------------------------------------------------------

# Introduction

This good-practice document is directed at archaeologists and
paleontologists working with microscopes, but anyone working with
microscope images might learn a few things here.

Microscopes now deliver digital images. “Digital images are data”
([Cromey 2013](#ref-cromey2013)). However, digital images are different
from analog images and from what the observer/analyst sees through the
oculars. Therefore, digital images have specific properties that must be
reported in publications, so that other researchers have the necessary
details to assess the published images and also so that they can
repeat/reproduce these images.

This document is by no means exhaustive and is limited in scope on
purpose, but I hope it will help many archaeologists and
paleontologists.

As a disclaimer, **this document only presents my opinion**, at least
for now. You are free to disagree. Whether you agree or not, I would
really appreciate if you could share your opinion and
[contribute](#how-to-contribute) to the development of this document, so
that it can be accepted by a larger community.

------------------------------------------------------------------------

# Scale of observation

A microscope is obviously used to observe features of an object that are
too small to be visible to the naked eye. To do so, a series of lenses
magnifies the object so that the analyst sees more details. But which
scale(s) is (are) appropriate and how to reach this (these) scale(s)
with a microscope?

So, the first question the analyst should ask is: **What is the size of
the features of interest?** It is important to consider the range of
sizes: the size of the smallest features is important, but so is the
size of the largest. This is because the larger this range, the less
likely it is that all these sizes can be observed with a single set of
settings. In other words, if features of different sizes are of
interest, several acquisitions at different scales will probably be
needed.  
Finding the size(s) of the features is often done directly during
observation: increasing the magnification until the features of interest
are visible. This is a valid approach if the microscope used has the
appropriate hardware (objectives, zoom, camera, etc.) to resolve the
features of interest. But it can also happen that the features of
interest are smaller or larger than what is permitted by the hardware at
hand. Moreover, when dealing with digital images, some other issues
might occur. This is why it is always advisable to start with at least a
rough idea of the size(s) of the features and of the capabilities of the
microscope(s) available to the analyst.

But how do we know what the microscope’s hardware can achieve in terms
of scale? Most publications and reports talk about *magnification*. But
what is it really and what does it mean? In the next section, I will
argue that magnification is pretty much useless in digital microscope
imaging and actually only confuses the analyst. Resolution is much more
important, but it is unfortunately still cryptic to many analysts; I
will therefore try to explain some concepts afterwards.

------------------------------------------------------------------------

# Magnification

Magnification is simply: the size of the magnified area divided by the
real size of the imaged sample’s area.

## Optical magnification

But let us first have a look at the optical magnification.  
The optical magnification of a microscope image when observed through
the oculars is straightforward to calculate:

$optical \ mag. = objective \ magnification \times ocular \ magnification \times optical \ zoom$
(1)

For example, using a 20 $\times$ objective with 10 $\times$ oculars and
2 $\times$ optical zoom, the total optical magnification is 400
$\times$.

## Digital magnification

Things get more complicated in the digital world. It all comes down to
one single question: **what is THE size of the magnified area when
stored on a digital image?** Is it the size of the screen when you
acquire the image? Is it the size of the screen when you view the image?
Is it the size printed on paper, or projected to a screen? There is no
single size for a digital image because it depends on the viewing
medium: increase the size of the viewing medium and the magnification
will increase as well, even though the image is the same. Does that mean
that increasing the size of the viewing medium will improve the
resolution? Unfortunately, no, as we will see below.

Let us see how the digital magnification is calculated. The problem with
a digital image (as opposed to an analog image) is that many components
come into play to magnify the sample: all the optical (objective,
optical zoom and camera adaptor) and digital (camera sensor, viewing
medium and digital zoom) components must be considered. Note that the
oculars are not relevant anymore because the light goes to the camera
without passing through the oculars.  
This is how to calculate the digital magnification:

$digital \ mag. = \frac{objective \ magnification \times optical \ zoom \times camera \ adaptor \times viewing \ medium \ diagonal \times digital \ zoom}{camera \ sensor \ diagonal}$
(2)

For example, using a 20 $\times$ objective, 2 $\times$ optical zoom, 1
$\times$ camera adaptor, 381 mm or 15” screen diagonal (to be precise,
what matters is the diagonal of the part of the screen where the image
is displayed), 1 $\times$ digital zoom, and 11 mm camera sensor
diagonal, the total on-screen magnification is:

$\frac{20 \times 2 \times 1 \times 381 \times 1}{11} \approx 1385 \times$

As you can see, with the same optical components (except oculars) as in
the example calculation of the optical magnification above (see formula
(1)), the resulting digital magnification is about 3.5 $\times$ larger
than the optical magnification. **So digital and optical magnifications
*are* different!**

An example I like to show is the figure 8a of Pedergnana
([2020](#ref-pedergnana2020)) (the paper can be read
[here](https://rdcu.be/cWpDH)). According to the legend, the original
magnification of the optical light microscopy image on the left is 10
$\times$ and that of the SEM image on the right is 200 $\times$
(actually 260 $\times$ according to the data zone on the image itself).
So different magnifications but same field of view and roughly same size
on the PDF…?! Here I do not mean that Antonella Pedergnana was wrong; on
the contrary, she actually did **correctly** report the microscopes’
settings **as it should be done**. She even specified in the legend that
the reported magnifications are ‘original magnifications’ to highlight
the fact that the images in the PDF have other (digital) magnifications.
The problem is that this acquisition setting can be misleading for the
non-expert reader. This example demonstrates that the concept of digital
magnification is troublesome, to say the least!

Also, the formula (2) shows that calculating the total digital
magnification is not so easy in practice: the camera sensor diagonal and
the viewing medium diagonal are not always known.

## Banning magnification?

So what now? **Should we all forget about magnification in digital
microscopy?** Well, pretty much, in my opinion.

**If the analyst has observed and analyzed while looking through the
ocular, the optical magnification is very relevant and should be
reported** (see section [Reporting and
sharing](#reporting-and-sharing)). However, the image published is a
digital one. This implies that the analyst and the readers/audience will
observe the sample at different magnifications (and resolutions as well,
see section [Resolution](#resolution)). In some cases, the
readers/audience might not be able to see what the analyst is referring
to. This might result in misunderstanding and potentially even disbelief
in respect to the analyst. Even when the analyst analyzed the digital
image directly, the viewing medium diagonal might change for each person
anyway (laptop screen vs. desktop screen vs. projected screen
vs. printed…).

As a side note, the field of view of a digital image is usually smaller
(to avoid [vignetting](https://en.wikipedia.org/wiki/Vignetting)) than
the field of view of the image as seen through the oculars, and the
contrast and clarity when looking through the oculars is usually much
better than any digital image. These are other sources of differences
when the analyst observed through the ocular but reports/publishes a
digital image.

There is another reason for avoiding the digital magnification. When I
was tasked to compare different digital microscopes (*i.e.* microscopes
without oculars and where the image is directly and only viewed on a
screen), I noticed that there were very large variations in the
magnification ranges advertised by the different manufacturers. Looking
at the small print, I realized that, for example, one manufacturer
reported the magnification as seen on a 15” screen diagonal, while
another one as seen on a 17.5” screen diagonal. This made sense because
this was the size of the image as seen in the respective acquisition
software packages. But this is very confusing to the buyer/user.  
Just for the comparison, let us simply change the screen from 15” to
17.5” (444.5 mm) in the example above:

$\frac{20 \times 2 \times 1 \times 444.5 \times 1}{11} \approx 1616 \times$

So this makes a significant difference!

There is another similar example, namely in SEM imaging. When using an
SEM, only the digital magnification is availble, but it is given
relative to a *reference*. For example, in the case of our Zeiss EVO 25,
the magnification is given relative to the Polaroid 545 format (other
formats can be selected), *i.e.* as if printed on 4 $\times$ 5” polaroid
paper. This used to be the printing format for analog images in the days
before digital SEMs. Note that other manufacturers might use different
references so the magnifications might not be comparable, once again,
and I am not sure all users know about this reference.

## Scale bar

So, if the digital magnification is useless, how can we know the size of
a digital microscope image? The good old **scale bar**! The field of
view, *i.e* the size of the imaged area of the sample, or rulers or
anything similar will do the trick too.

One would expect that everybody knows that a scale bar (or some form of
scaling) must be provided with each image. Yet, “\[a\]pproximately half
of papers in physiology (49%) and cell biology (55%) and 28% of plant
science papers provided scale bars with dimensions (in the figure or
legend) for all images in the paper \[…\]. Approximately one-third of
papers in each field contained incomplete scale information, such as
reporting magnification or presenting scale information for a subset of
images. Twenty-four percent of physiology papers, 10% of cell biology
papers, and 29% of plant sciences papers contained no scale information
on any image” ([Jambor et al. 2021, 3](#ref-jambor2021)).  
In sum, **only about half of the papers in these fields publish
microscope images with proper scaling information; this is not much!** I
do not expect that archaeology is any different, although I am not aware
of such a survey for archaeology.

------------------------------------------------------------------------

# Resolution

**In general, *resolution* refers to the level of details that can be
observed. In other words, it defines the size of the smallest observable
features.**

There is not one single resolution but many different, complementary
definitions of resolution. First, it is important, once again, to
differentiate between optical and digital resolutions. And second, there
are lateral (XY) and vertical (Z) resolutions.

Most terms and definitions here refer to the [Fair Data Sheet
Initiative, v1.2α](http://www.optassyst.de/fairesdatenblatt/) (the
website is only in German, but the Fair Data Sheet itself has an English
version). I will abbreviate it “FDS”.

## Optical lateral resolution

Due to aberrations from the optics and diffraction of the light, an
optical system will be limited in its ability to distinguish points; the
image will become blurry at the smallest scales. These effects are the
basis for the calculation of the optical lateral resolution as defined
by the [Rayleigh
criterion](https://en.wikipedia.org/wiki/Angular_resolution).

The calculated optical lateral resolution is the “minimum theoretical
distance between two adjacent, barely distinguishable features of an
object” (FDS §2.2.8). In other words, if two points are closer from each
other than the optical lateral resolution, then it is not possible to
distinguish them (*i.e.* they will look like one point only). They will
appear as two separate points only if they are further from each other
than the optical lateral resolution.

The calculated optical lateral resolution $\delta_L$ depends on the
numerical aperture of the optics (= objective + optical zoom, $NA$), on
the wavelength of the light $\lambda$ and on a factor $K$:

$\delta_L = \frac{K.\lambda}{NA}$ (3)

The value of $K$ is 0.61 for bright field microscopy (= “classical”
light microscopes). For laser-scanning confocal microscopy, $K$ depends
on the diameter of the pinhole and varies between 0.37 and 0.61
([Artigas 2011](#ref-artigas2011)).

From formula (3) and the definition of the optical lateral resolution,
it becomes apparent that **the smaller** $\delta_L$, the better the
resolving power of the microscope (*i.e.* closer points will be
distinguishable). This is what we usually refer to as “*higher*
resolution”, even though the value for $\delta_L$ is *smaller*.
Confusing, right? This is why **I prefer to talk about “better/worse”
resolution rather than “smaller/larger”**.

The NOTE 3 of the FDS §2.2.8 states that “the optical \[lateral\]
resolution can be achieved only under ideal conditions (including
complete illumination of the pupil) on planar objects. This value is
usually not reached on textured surfaces”. In archaeology and
paleontology, we usually deal with textured surfaces!

## Digital lateral resolution

The digital lateral resolution, or *measuring point spacing*, is the
“sampling interval of measuring points in the measuring volume, both in
X and in Y direction” (FDS §2.2.7). This is also referred to as the
*pixel size* (although *pixel size* or *pixel pitch* can also refer to
the size of the photodiodes on the detector/camera, which is a fixed
value independent of the field of view) or *spatial sampling*.

The measuring point spacing is calculated by dividing the *measuring
area* (FDS §2.2.1, also called *field of view*) by the *maximum number
of measuring points in a single measurement* (FDS §2.1.2, also called
*frame size* or *number of pixels*):

$measuring \ point \ spacing = \frac{measuring \ area}{number \ of \ pixels}$
(4)

## Digital zoom

Formula (2) includes the digital zoom in the calculation of the digital
magnification, but it is not part of formula (4) for the digital lateral
resolution. So what happens when zooming in *digitally*?

Let us start with an original image 100 $\times$ 100 µm with 1000
$\times$ 1000 pixels. This results in a measuring point spacing of 0.1
µm.  
The digital zoom acts like a cropping + enlarging tool: the original
image will be first cropped and then enlarged to the same viewing size
as the original image.  
A digital zoom factor 2 $\times$ means that the original image is
cropped by half in X and in Y directions, *i.e.* the zoomed image is 4
$\times$ smaller than the original image. This is true both for the size
in µm and for the number of pixels. The zoomed image will therefore be
50 $\times$ 50 µm but it will occupy the same space on your screen as
the original image (*i.e.* digital magnification 2 $\times$ larger). And
it will have 500 $\times$ 500 pixels.  
So what about the digital lateral resolution of the zoomed image? 0.1
µm, just like the original image.

All this to say that the **digital zoom obviously changes the digital
magnification but does not influence the digital lateral resolution**.

Still, it seems that zooming in digitally helps to see more details.
This is just because the details are displayed larger on the screen, not
because they are better resolved. For a better digital resolution, a
smaller field-of-view for the same number of pixels, or more pixels for
the same field-of-view, is needed. This can be achieved by using a
higher magnification objective and/or an optical zoom, or a camera with
more pixels.

## Optical vertical resolution and depth of field

The optical vertical, or axial, resolution is equal to the depth of
field for a bright field (BF) microscope:

$\delta_A(BF) = depth \ of \ field = \frac{n.\lambda}{NA^2}$ (5)

with $n$ the refractive index of the medium; $n_{air} \approx 1$.

For a confocal microscope, the axial resolution is calculated by the
optical slice thickness, which also depends on the pinhole diameter
([Artigas 2011](#ref-artigas2011)):

$\delta_A(conf) = \frac{0.64 \lambda}{n- \sqrt{n^2-NA^2}}$ (6) with a
pinhole diameter $PH < 0.25 AU$ ([Airy
Unit](https://en.wikipedia.org/wiki/Airy_disk))

$\delta_A(conf) = \sqrt{(\frac{0.88 \lambda}{n- \sqrt{n^2-NA^2}})^2 + (\frac{n.PH.\sqrt{2}}{NA})^2}$
(7) with a pinhole diameter $PH$ $\ge 0.25 AU$

Here again, **the smaller** $\delta_A$, the better the resolution is.

## Digital vertical resolution

The digital vertical resolution is meaningless in case of a 2D image
(even for extended depth of focus - EDF - images) but it is relevant for
2.5 and 3D images.

The digital vertical resolution of a 2.5D image acquired from a confocal
microscope is better than the step size (*i.e.* the distance between the
individual images, or slices, of a stack) because of the way it is
processed (see [Artigas 2011](#ref-artigas2011)).  
In short, the focal distance is constant for a given objective, so when
the microscope’s objective moves up and down, different points of the
sample are in focus. Each point (pixel) on each slice records the
intensity of the signal (called axial response) at that location (X+Y
from stage coordinates and Z from the slice’s height). The intensity
increases when the focal plane gets closer to the point on the sample
and decreases again when the focal plane moves further away from the
point on the sample. The curve of the axial response (intensity)
vs. height of the slice therefore has a maximum that can be
mathematically computed (see fig. 11.6 in [Artigas
2011](#ref-artigas2011)) and that do not necessarily fall on the height
of a given slice. This maximum is the value used for the height of the
given pixel. Repeat the process for all pixels, and you get a 2.5D
height map with a digital vertical resolution better than what the
mecanics (drives or piezo) can achieve.

Unfortunately, I do not know how to calculate the digital vertical
resolution of a z-stack.  
If anyone knows more about it, please [contribute](#how-to-contribute)!

## Relationship between optical and digital resolutions

So far, so good, and not too complicated. The problem is that we now
have two different values for the lateral resolution and two others for
the vertical resolution. Which one(s) should we care about? All, of
course! But **what should the relationship between optical and digital
resolutions be?**

The Nyquist criterion (based on the [Nyquist–Shannon sampling
theorem](https://en.wikipedia.org/wiki/Nyquist%E2%80%93Shannon_sampling_theorem))
states that the value for the digital resolution should be 2-3 times
smaller (approx. 2.8 times smaller according to [Pawley
2006](#ref-pawley2006)) than the value for optical resolution. This is
necessary to digitally image with sufficient details the transition
between features that are optically visible.

This relationship holds true for both the lateral and the vertical
resolutions.  
In case of the lateral resolution, the relationship is between the
measuring point spacing and the optical lateral resolution.  
For example, if $\delta_L = 0.6 \ \mu m$, then the measuring point
spacing should be 0.2-0.3 µm, ideally 0.21 µm.  
In case of the vertical resolution, the relationship is between the step
size and the optical vertical resolution (*i.e* depth of field in
widefield or optical slice thickness in confocal).  
For example, if $\delta_A = 0.6 \ \mu m$, then the step size should be
0.2-0.3 µm, ideally 0.21 µm.

If the digital resolution is more than 3 $\times$ smaller than the
optical resolution, this will result in oversampling: adjacent pixels
will have the same values, so the digital image will not contain more
information but simply more data. This results in larger files than
necessary and generally does not improve the quality of the image. On
the contrary, it can even lead to worse images because each pixel will
record less signal (i.e. lower signal-to-noise ratio or SNR, [Pawley
2006](#ref-pawley2006)).  
If the digital resolution is less than 2 $\times$ smaller than the
optical resolution, this will result in undersampling: the transition
between features that are optically visible will not be visible on the
digital image.

There are many considerations to take into account in the analog to
digital conversion process, but as Pawley ([2006, 70](#ref-pawley2006))
wrote: “**If you don’t want to worry about any of this, stick to
Nyquist!**”

Note that in the section [Optical lateral
resolution](#optical-lateral-resolution), I argued that we should avoid
the terms “larger” and “smaller” when talking about resolutions. But in
this section, it is really about the relationship between the values of
$\delta_L$ and measuring point spacing, or $\delta_A$ and step size. In
any case, the relationship could also be stated that way: “the digital
resolution should be 2-3 $\times$ better than the optical resolution”.

------------------------------------------------------------------------

# Scale, magnification, resolution - summary

**Magnification and resolution are different concepts and are not
interchangeable. Resolution is given in a unit of length** (e.g. µm)**,
while magnification is without unit** (“$\times$”).

***Magnification* can be understood as an aid to see the *resolution*:
resolution will define what can be seen or not, while increasing the
magnification will make the visualization of the observable details
easier. This is why, in my opinion, talking about *resolution* is much
more useful and relevant than magnification, especially in the digital
world.**

***Scale* is a fundamental concept for any observation. Magnification is
often, unfortunately, used as a proxy for scale. However, magnification
is quite decoupled from scale. Scale can be properly described by field
of view** (FOV, i.e. the size of the region observed) **and resolution**
(i.e. the level of details visible on the optical and digital images)**.
Magnification informs only on the FOV, but even for that, it is not very
useful when most microscopes now allow for stitching in order to
increase the FOV at constant magnification and resolution.**

As a side note for use-wear analysts, the two approaches to use-wear
analysis are called *high-power* and *low-power*, not
*high-magnification* and *low-magnification*!

**In summary, forget about magnification and learn about resolution!**

When planning your microscope documentation, it is important to choose
the equipment according to your imaging needs: what is the size of the
smaller features that your are trying to document? Based on that, what
resolution would you need and in-turn, which microscope and objective?  
There are of course many other considerations (sample size, sample
topography, objective working distance, etc.), but thinking about the
needs in resolution is a good start!

------------------------------------------------------------------------

# Processing

Few images are published without some form of processing. Sometimes,
processing is even necessary to create (e.g. EDF, stitching, topography
reconstruction) or analyze (e.g. contrast/brightness, wavelength
filters) the image. Even the raw data output by every instrument are
processed to some degree.  
While processing deserves a whole good-practice document on its own, I
would just like to give some general advices here that will hopefully be
applicable to most processing routines. But feel free to
[contribute](#how-to-contribute) for more!

## Definitions

Following the definitions of Aaron and Chew ([2021, 1](#ref-aaron2021)),
*processing* “serves to digitally transform an acquired dataset by
enhancing or isolating signals of interest and/or suppressing other
signals and noise that will otherwise prevent accurate analysis”.
*Analysis* refers to “a vast set of diverse approaches to extract \[…\]
meaningful, quantitative measurements from a dataset”. Lastly,
*pre-processing* includes the “steps that are required to be taken
before image data can be properly processed \[…\]. Such steps generally
do not serve to enhance particular features in an image per se, but
rather correct for imperfections commonly encountered in imaging
systems.”

Here are some examples in each category when considering surface texture
analysis (dental microwear texture analysis or quantitative artifact
microwear analysis):

- pre-processing: topography reconstruction from a Z-stack, stitching…  
- processing: leveling, form removal, thresholding, wavelength
  filters…  
- analysis: texture analysis following ISO 25178, scale-sensitive
  fractal analysis, furrow analysis…

In the remaining of this section, I will use the term processing to
include both pre-processing and true processing. This makes the
sentences easier to read and the discussion applies to both anyway.

## Recommendations

Even if we sometimes tend to assume that there is only one way to
process an image, there are in fact often several methods or algorithms
to do so, and there are always various settings to adjust. Additionally,
some processing happens before you get the raw data from the instrument.
Lastly, “\[a\]s images are numerical data, image processing invariably
changes these data and thus needs to be transparently documented”
([Schmied et al. 2023, 7](#ref-schmied2023)). This is why it is
important to **be as precise as possible when reporting about the
acquisition and processing** (see section [Reporting and
sharing](#reporting-and-sharing)).

It is also crucial to **process all images of a dataset in the same
way**. This might seem obvious, but different processing methods might
produce results that might appear identical/similar even if they
actually are different. Processing all images in the same way ensures
that all images are comparable at least within a dataset. Of course,
this is true only if **the images were acquired in the same way**!  
So, while the details are more nuanced, I believe the message is clear
and every analyst should try his/her/their best to acquire and process
images and data in a consistent and comparable manner.

Another general piece of advice is to **keep the raw data**, in this
case the acquired image, and to **process a copy** of it rather than
overwriting the acquired image (see e.g. [Cromey 2013](#ref-cromey2013);
[Schmied and Jambor 2021](#ref-schmied2021)). This way, it is possible
to check the result and process differently if necessary. See section
[Saving](#saving) for a discussion on raw/derived data and file formats.

Last but not least, it is important to **keep a very detailed record of
the processing and analysis steps that were performed**. Templates and
scripts will make it easier to repeat and reproduce the
processing/analysis. This is not only important to share data (see
section [Sharing](#sharing)); it is also important for yourself as it is
likely that you will have to repeat the analysis at some point, at least
for some images. [protocols.io](https://www.protocols.io/) can be a
useful tool for this.

[Fiji/ImageJ](https://imagej.net/) is a great, open-source tool for
image analysis. Schmied and Jambor ([2021](#ref-schmied2021)) proposed
guidelines for image analysis and a processing workflow in Fiji; there
is no reason not to follow and use them! The checklists of Schmied et
al. ([2023](#ref-schmied2023)) are also very useful.

------------------------------------------------------------------------

# Saving

## Raw vs. derived data

I totally agree with Ben Marwick and colleagues that raw data should be
kept raw and clearly separated from derived data (e.g. [Marwick and
Pilaar Birch 2018](#ref-marwickpilaar2018); [Marwick, Boettiger, and
Mullen 2018](#ref-marwicketal2018)).

Still, it is not always clear to distinguish between the two, nor
practicable to keep the raw(est) data. For example, the raw data of an
EDF image or a 2.5D topographical model (= height map, e.g. from a
confocal microscope) is a Z-stack. Z-stacks can be very large files so
keeping all these Z-stacks requires a lot of storage space. While
storage is not really limiting anymore, the environmental impacts of
data centers and online repositories cannot be ignored (e.g. [Samuel and
Lucivero 2020](#ref-samuel2020)).

Also the derived data of an analysis can be the raw data of another.
Using the example of surface texture analysis (dental microwear texture
analysis or quantitative artifact microwear analysis), the raw data of
the analysis are the height maps (which are themselves derived from
pre-processing the Z-stacks) that are used as input for MountainsMap (or
equivalent) to calculate the surface texture parameters for each height
map, which are eventually exported into a CSV file. This CSV file is
in-turn the raw data for the subsequent statistical analysis.

All this to say that the decision should be made on a case-by-case basis
about what data is raw and what is derived. Nevertheless, there are some
general principles that apply in most (all?) cases. Make sure to:

- **save the rawest data possible**, usually the acquired, unprocessed
  image;  
- **save every derived data that is included in the final analysis**
  (i.e. input data of the results), especially if the
  processing/analyses are not fully automatized;  
- **save all the metadata** associated with both the raw and derived
  data (see section [File formats and
  software](#file-formats-and-software));  
- **save in appropriate format(s)** (see section [File formats and
  software](#file-formats-and-software)).

## File formats and software

For long-term usability, accessibility and sustainability, proprietary
formats (i.e. files that can only be opened with a paid software) should
be avoided and **stable, open, non-proprietary formats should be
preferred**. The DANS maintains a [list of preferred and non-preferred
formats](https://dans.knaw.nl/en/file-formats/). **For microscopy
images, the [OME-TIFF
format](https://docs.openmicroscopy.org/ome-model/6.3.1/ome-tiff/index.html)
has become the standard.**

Most microscope manufacturers offer software packages to acquire images;
in some cases, these software packages are even necessary to operate the
microscopes. Not all of these software packages can save in an open
format, even less so in OME-TIFF. Unfortunately, metadata sometimes get
lost when the image is not saved in the native, proprietary format.  
This is why, if your acquisition software cannot natively save in an
open format, ***I*** **would recommend to save the image in the
proprietary format** (in order to save all the metadata) **and to
additionally export to an open format** (for long-term accessibility).
Sometimes, it is also possible to export the metadata into an open
format (e.g. JSON, XML, CSV or TXT).

Following on this discussion, it is therefore important to favor
open-source software packages over paid ones. Nevertheless, open-source
projects often have difficulties to keep running and being developed
(see e.g. [Coelho and Valente 2017](#ref-coelho2017)). Also, open-source
software packages are often less user-friendly, and are slower to add
new functionalities and to adapt to OS upgrades. So, open-source is not
always better.  
Still, [Fiji/ImageJ](https://imagej.net/) is a great open-source
solution for image analysis with a 25-year-long history (meaning it is
likely to survive).
[Bio-Formats](https://www.openmicroscopy.org/bio-formats/) is an
important “software tool for reading and writing image data using
standardized, open formats”, which is incorporated into ImageJ. Check
the [how-to ImageJ2-Fiji](/How-tos/ImageJ2-Fiji.md) for details on how
to read Zeiss files and access their metadata with this software.  
Some microscope manufacturers also offer a free viewer or a free light
version (e.g. Zeiss’ [ZEN
starter](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-starter.html)
and [ZEN
lite](https://www.zeiss.com/microscopy/en/products/software/zeiss-zen-lite.html)).

## JPEG, PNG, TIFF, RAW

Following up on the previous section, every one of us has wondered at
least once which image format should be preferred and what the
differences are between JPG, JPEG, PNG, TIF and TIFF. Here, I will try
to give an overview and general recommendations. This section concerns
only raster image formats, as microscope images are always raster
images.

I recommend reading the documentation about the different [raster file
formats](https://www.adobe.com/creativecloud/file-types/image/raster.html)
on the Adobe website, which is, in my opinion, clear and detailed.

- [TIFF](https://www.adobe.com/creativecloud/file-types/image/raster/tiff-file.html)
  (.tif or .tiff, same format but different extensions for historical
  reasons) is the format to choose if you want to save images at full
  resolution and with best quality, which in turn implies that TIFF
  files are large. Metadata can be saved together with the image when
  using this format (e.g. for SEM images).  
- [JPEG](https://www.adobe.com/creativecloud/file-types/image/raster/jpeg-file.html)
  (.jpg or .jpeg, same format but different extensions for historical
  reasons) is a widely used format for photos. Files are small and of
  generally good quality, but the lossy compression means that some
  details are lost. JPEG files can include metadata, especially the
  camera’s [EXIF data](https://en.wikipedia.org/wiki/Exif), but is not
  recommended for scientific imaging ([Cromey 2013](#ref-cromey2013)).  
- [PNG](https://www.adobe.com/creativecloud/file-types/image/raster/png-file.html)
  is best knowned for their transparent backgrounds, but it is also a
  good format for any type of image thanks to its lossless compression.
  Files are smaller than TIFF but larger than JPEG. While many users
  tend to prefer JPEG, I think PNG could be better for many applications
  and should be preferred to JPEG ([Cromey 2013](#ref-cromey2013);
  [Schmied and Jambor 2021](#ref-schmied2021); [Schmied et al.
  2023](#ref-schmied2023)). Compare the two formats
  [here](https://www.adobe.com/creativecloud/file-types/image/comparison/jpeg-vs-png.html).  
- I am not aware of any microscope camera that can save in
  [RAW](https://www.adobe.com/creativecloud/file-types/image/raw.html),
  but DSLR cameras can usually do it. So this format is worth
  considering for users who have a DSLR camera mounted on the phototube.

------------------------------------------------------------------------

# Reporting and sharing

**“The underlying premise of image publication and ethics guidelines is
that a digital image is data and that the data should not be manipulated
inappropriately”** ([Cromey 2013, 5](#ref-cromey2013)).

All the background information of the previous sections aims at
providing the required knowledge to use a microscope to reach the
desired scale of observation and to save all the acquired data and
metadata. While it is important for the analyst to see what he/she/they
want to see on the sample, it is equally important that the
reader/audience that will be presented - or even will assess - the work
is able to know what can be observed in terms of scale on the
reported/published/shared images. This is also important for
*repeatability* and *reproducibility* (and *pre-producibility* *sensu*
[Stark 2018](#ref-stark2018)).

The importance of reporting for microscopy is not unique to
archaeology/paleontology (see e.g. [Calandra et al.
2019](#ref-calandra2019)) and other fields also suffer from a lack of
high-quality reporting (see e.g. [Marqués, Pengo, and Sanders
2020](#ref-marqués2020) in biomedical research).

A large community of researchers in life sciences are working on
guidelines for reporting microscope data (e.g. [Aaron and Chew
2021](#ref-aaron2021); [Hammer et al. 2021](#ref-hammer2021);
[Heddleston et al. 2021](#ref-heddleston2021); [Jambor et al.
2021](#ref-jambor2021); [Ryan et al. 2021](#ref-ryan2021); [Sarkans et
al. 2021](#ref-sarkans2021); [Schmied et al. 2023](#ref-schmied2023), as
well as the [Open Microscopy Environment -
OME](https://www.openmicroscopy.org/about/), the [European Light
microscopy initiative - ELMI](https://elmi.embl.org/home/our-aims/), the
[Society for Microscopy and Image Analysis -
GerBI-GMB](https://gerbi-gmb.de/society/) and the [Quality Assessment
and Reproducibility for Instruments & Images in Light Microscopy -
QUAREP-LiMi](https://quarep.org/about/) communities). The work they do
is incredible, but unfortunately, it concerns mostly life sciences and
some aspects are not relevant to archaeology, while some others relevant
to archaeology are not addressed.  
Nevertheless, the Bare Minimal Microscopy Reporting Requirements
Checklist by the QUAREP ([Montero Llopis et al.
2025](#ref-monterollopisQUAREPBareMinimal2025)) offer a good starting
point.

## Minimum reporting requirements

Below is a list of what I think is necessary for pre-producible
microscope images. This list should be adapted according to the
equipment/software used.

| **Number** | **Category**                | **What**                                                                          | **Why**                                                                                  | **How? (examples)**                                                                                                                                                                                                    |
|------------|-----------------------------|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1          | Observation/analysis method | Observation/analysis through oculars or directly on the digital image?            | To know how the analyst performed the analysis                                           | “The features were observed and analyzed through the oculars. The images reported are therefore not equivalent to what has been observed during analysis.”                                                             |
| 2          | Microscope                  | Manufacturer and model of the microscope                                          | To account for all (unknown) settings that are part of the microscope’s design           | “AxioScope.A1 (Carl Zeiss Microscopy GmbH)”                                                                                                                                                                            |
| 3          | Technique                   | Imaging technique / contrast                                                      | To interpret the image according to the technique(s) used                                | “Confocal microscopy” or “bright field” or “DIC”                                                                                                                                                                       |
| 4          | Light                       | Illumination                                                                      | To interpret the image according to the illumination(s) used                             | “Ringlight illumination” or “Coaxial illumination”                                                                                                                                                                     |
| 5          | Light                       | Type + wavelength of the light source                                             | To calculate the optical resolutions                                                     | “Violet LED 405 nm”                                                                                                                                                                                                    |
| 6          | Light                       | Light source intensity                                                            | To be able to repeat the acquisition                                                     | “60%”                                                                                                                                                                                                                  |
| 7          | Light                       | Exposure time                                                                     | To be able to repeat the acquisition                                                     | “100 ms”                                                                                                                                                                                                               |
| 8          | Optics                      | Objective specifications                                                          | To calculate the optical magnification (if applicable, see \#1) and optical resolutions  | “Objective Zeiss C Epiplan-Apochromat Mag. = 50 $\times$ / NA = 0.95 / WD = 0.22 mm”                                                                                                                                   |
| 9          | Optics                      | Oculars magnification, if applicable (see \#1)                                    | To calculate the optical magnification                                                   | “10 $\times$ oculars”                                                                                                                                                                                                  |
| 10         | Optics                      | Optical zoom, if applicable (see \#1)                                             | To calculate the optical magnification                                                   | “2 $\times$ optical zoom”                                                                                                                                                                                              |
| 11         | Camera                      | Measuring point spacing + field of view + number of pixels (at least two of them) | To calculate the digital lateral resolution                                              | “100 $\times$ 100 µm for 1000 $\times$ 1000 pixels” or “1000 $\times$ 1000 pixels, measuring point spacing = 0.1 µm”                                                                                                   |
| 12         | Camera                      | Scale bar                                                                         | To visualize the size of the imaged region                                               | “Scale bar = 100 µm”                                                                                                                                                                                                   |
| 13         | Confocal                    | Pinhole diameter, if applicable                                                   | To calculate the optical resolutions                                                     | “PH = 54 µm (1 AU)”                                                                                                                                                                                                    |
| 14         | Confocal                    | Step size + z-range, if applicable                                                | To be able to repeat the measurement                                                     | “40-50 µm with 0.2 µm steps”                                                                                                                                                                                           |
| 15         | Confocal                    | Temperature + humidity during topography scanning, if possible                    | T & H can influence the fine-scale measurements of topography                            | “Scans were acquired at 20 \< T \< 22 °C and 50 \< rH \< 70 %”                                                                                                                                                         |
| 16         | Confocal                    | Location of the equipment                                                         | An environment without vibrations is necessary for fine-scale measurements of topography | “The confocal microscope is located in the basement and placed on a passive anti-vibration table, itself placed on a concrete based decoupled from the rest of the floor”                                              |
| 17         | Confocal                    | Any other equipment-specific setting                                              | To be able to repeat the measurement                                                     | “Master gain = 220 V”                                                                                                                                                                                                  |
| 18         | Software                    | Versions of acquisition, processing and analysis software packages                | Different versions might produce different results                                       | “ZEN blue 3.5 Hotfix 7 (Carl Zeiss Microscopy GmbH) with module Shuttle-and-Find” or “ConfoMap 9.2.10042 with module Scale-sensitive Analysis (Digital Surf)”                                                          |
| 19         | Pre-processing              | Stitching, if applicable                                                          | To be able to repeat the processing                                                      | “2 $\times$ 2 tile regions were acquired, with shading correction (to avoid seeing the separations between single images), 5% minimal overlap and 10% maximal shift, ‘optimized’ comparer and ‘best’ global optimizer” |
| 20         | Pre-processing              | Extended depth of focus (EDF), if applicable                                      | To be able to repeat the processing                                                      | “Z-stacks were processed to EDF images with the wavelets method and without z-stack alignment”                                                                                                                         |
| 21         | Processing/Analysis         | Image enhancements / filters / image analysis settings, if applicable             | To be able to repeat the processing                                                      | “The contour were enhanced with settings A and B; and brightness, contrast and gamma were adjusted to C, D and E respectively”                                                                                         |
| 22         | Processing/Analysis         | Workflow and settings of the surface texture analysis, if applicable              | To be able to repeat the processing                                                      | “The surface texture analysis was performed with the following template \[add analysis details and link to template\]”                                                                                                 |

From my point of view, **all of these pieces of information should be
published together with every microscope acquisition**.

I would like to stress that most of these metadata are generated and
saved automatically together with the image data (at least when you use
the appropriate format) so that there is no extra work needed to compile
the image metadata beyond sharing (see section [Instrument-specific
guidelines](#instrument-specific-guidelines)). I therefore do not see a
reason why we should not report them.

Additionally, I recommend **following the guidelines of Jambor et al.
([2021](#ref-jambor2021)) to improve the quality of the images
themselves, as well as using the checklists of Schmied et al.
([2023](#ref-schmied2023)) to make sure that at least the relevant
“minimal” requirements are met** (but aim for the “ideal”
requirements!).

## Sharing

A lot could be said about data sharing and Open Science. I will keep it
brief here and focused on microscope images; more general and extensive
discussions can be found in e.g. Marwick and Pilaar Birch
([2018](#ref-marwickpilaar2018)), Gomes et al. ([2022](#ref-gomes2022)),
and Karoune and Plomp ([2022](#ref-karoune2022)).

**In my opinion, publishing only a few, supposedly representative images
of the whole dataset is not enough** because of the following reasons:

1.  The sample might be representative in some aspects but not in
    others.  
2.  To be honest, in most cases, only the “nicest” images are published
    and the least informative/relevant are not; this implies a strong
    bias and the true signal might just be lost by this selective
    sampling/reporting.  
3.  Images published in a journal article or in a book are usually small
    and of reduced quality (in the PDF at least), so the published
    images might not even show what can be seen on the full-resolution
    image.  
4.  Without seeing all images in full resolution, how can anyone assess
    whether the data support the conclusions?  
5.  It would be a shame to keep all these images for yourself.  
6.  Why should we show only a small part of the extensive work we did?
    Let us do ourselves a favor and show how hard we work!

Or as Cromey ([2013, 3](#ref-cromey2013)) puts it: “If we only show
other people the pictures we want them to see, then the viewers will
most likely reach the interpretation that we want them to have. What if
our interpretation is wrong? It may be a poorly kept secret that most
published images are somewhat less than “representative”, but is this
right? What would happen to the quality of science if we only showed our
most compelling images to our project leaders, lab group, or
collaborators?”

**I would therefore recommend:**

1.  **to keep showing a sample as representative as possible in the
    journal article, but**  
2.  **to additionally upload all images with their metadata to an online
    repository**.

I would like to stress that the data should be uploaded to a trustworthy
online repository (e.g. [Zenodo](https://zenodo.org/),
[OSF](https://osf.io/) or [Figshare](https://figshare.com/)), rather
than as online supplementary information (SI) to the article. This is
because SI might be behind a paywall, just like the article. Even when
it is not, publishers might have restrictions about file formats and
names. And since everyone does mistakes, it is easier to correct them if
you have access to the repository rather than relying on the publisher
to do it (which can take a long time or might even never happen).  
Ideally, data should be uploaded to a discipline-specific repository
rather than a generalist repository like Zenodo or OSF. But I am not
aware of any archaeology-specific repository that is commonly used. I
have heard about for example The Digital Archaeological Record
([tDAR](https://core.tdar.org)) but it seems to be mostly used for
excavation data. Please [contribute](#how-to-contribute)!

Here again, the discussion about raw/derived data and file formats is
important (see section [Saving](#saving)): both raw and derived data
should be shared in formats that include all the metadata ([Schmied et
al. 2023](#ref-schmied2023)).

I propose step-by-step instructions to upload files to Zenodo in [how-to
Zenodo](/How-tos/Zenodo.md).

## Instrument-specific guidelines

I have tried to make it easy for the users of the **Im**aging
**P**latform **a**t **L**EIZ**A**
([IMPALA](https://www.leiza.de/forschung/infrastrukturen/labore/impala)):
a [Shiny App](https://shiny.rstudio.com/) guides the users to fill in
the required information and exports the report to an XLSX or ODS file
that can be shared together with the images (see section
[Sharing](#sharing)). This App is still in development and is part of
the repository
[imaging-reports](https://github.com/ivan-paleo/imaging-reports) on
GitHub.

To complement this, I have prepared guidelines specific to the
instruments we have at the IMPALA in the folder
[Guidelines](/Guidelines/). The guidelines include text snippets that
can be copy/pasted/edited for the method section of a publication and
have been converted from Markdown to DOCX format using the extension
[vscode-pandoc](https://marketplace.visualstudio.com/items?itemName=DougFinke.vscode-pandoc).
They also explain in details what type of data should be shared and
how.  
Feel free to [contribute](#how-to-contribute) guidelines for other
instruments!

**Neither the reports nor the text snippets are meant to be used for
every acquisition. Instead, they serve to summarize the acquisition and
analysis processes and should be used only once for each
publication/project.**  
**But this works well only in combination with the detailed metadata
shared together with the data themselves**, as detailed in the
guidelines (see also section [Sharing](#sharing)).

------------------------------------------------------------------------

# How to contribute

I appreciate any comment from anyone (expert or novice) to improve this
document, so do not be shy! There are three possibilities to contribute.

1.  Submit an issue: If you notice any problem or have a question,
    submit an
    [issue](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues).
    You can do so
    [here](https://github.com/ivan-paleo/publish-micro-image/issues).  
    A GitHub account is necessary.

2.  Propose changes: This document is written in
    [Quarto](https://quarto.org/). If you know how to write in this
    format, please propose text edits as a [pull
    request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests)
    (abbreviated “PR”).  
    A GitHub account is necessary.

3.  Send me an email: If you do not have a GitHub account and do not
    want to sign up, you can still write me an email (Google my name
    together with my affiliation to find my email address).

By participating in this project, you agree to abide by our [code of
conduct](CONDUCT.md).

------------------------------------------------------------------------

# License

[![CC BY-NC-SA
4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

This work is licensed under a [Creative Commons
Attribution-NonCommercial-ShareAlike 4.0 International
License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

See also [License file](LICENSE) in the repository.

Author: Ivan Calandra

[![CC BY-NC-SA
4.0](https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

License file, badge and image from Soler ([2022](#ref-soler2022)).

------------------------------------------------------------------------

# References

<div id="refs" class="references csl-bib-body hanging-indent"
entry-spacing="0">

<div id="ref-aaron2021" class="csl-entry">

Aaron, Jesse, and Teng-Leong Chew. 2021. “A Guide to Accurate Reporting
in Digital Image Processing Can Anyone Reproduce Your Quantitative
Analysis?” *Journal of Cell Science* 134 (6): jcs254151.
<https://doi.org/10.1242/jcs.254151>.

</div>

<div id="ref-artigas2011" class="csl-entry">

Artigas, Roger. 2011. “Imaging Confocal Microscopy.” In, edited by R.
Leach, 237–86. Berlin, Heidelberg: Springer Berlin Heidelberg.
<https://doi.org/10.1007/978-3-642-12012-1_11>.

</div>

<div id="ref-calandra2019" class="csl-entry">

Calandra, Ivan, Lisa Schunk, Konstantin Bob, Walter Gneisinger,
Antonella Pedergnana, Eduardo Paixao, Andreas Hildebrandt, and Joao
Marreiros. 2019. “The Effect of Numerical Aperture on Quantitative
Use-Wear Studies and Its Implication on Reproducibility.” *Scientific
Reports* 9 (1): 6313. <https://doi.org/10.1038/s41598-019-42713-w>.

</div>

<div id="ref-coelho2017" class="csl-entry">

Coelho, Jailton, and Marco Tulio Valente. 2017. “ESEC/FSE’17: Joint
Meeting of the European Software Engineering Conference and the ACM
SIGSOFT Symposium on the Foundations of Software Engineering.” In,
186–96. Paderborn Germany. <https://doi.org/grmgjz>.

</div>

<div id="ref-cromey2013" class="csl-entry">

Cromey, Douglas W. 2013. “Digital Images Are Data: And Should Be Treated
as Such.” In, edited by Douglas J. Taatjes and Jürgen Roth, 1–27.
Methods in Molecular Biology. Totowa, NJ: Humana Press.
<https://doi.org/10.1007/978-1-62703-056-4_1>.

</div>

<div id="ref-gomes2022" class="csl-entry">

Gomes, Dylan G. E., Patrice Pottier, Robert Crystal-Ornelas, Emma J.
Hudgins, Vivienne Foroughirad, Luna L. Sánchez-Reyes, Rachel Turba, et
al. 2022. “Why Don’t We Share Data and Code? Perceived Barriers and
Benefits to Public Archiving Practices.” *Proceedings of the Royal
Society B: Biological Sciences* 289 (1987): 20221113.
<https://doi.org/grbx5m>.

</div>

<div id="ref-hammer2021" class="csl-entry">

Hammer, Mathias, Maximiliaan Huisman, Alessandro Rigano, Ulrike Boehm,
James J. Chambers, Nathalie Gaudreault, Alison J. North, et al. 2021.
“Towards Community-Driven Metadata Standards for Light Microscopy:
Tiered Specifications Extending the OME Model.” *Nature Methods* 18
(12): 1427–40. <https://doi.org/10.1038/s41592-021-01327-9>.

</div>

<div id="ref-heddleston2021" class="csl-entry">

Heddleston, John M., Jesse S. Aaron, Satya Khuon, and Teng-Leong Chew.
2021. “A Guide to Accurate Reporting in Digital Image Acquisition Can
Anyone Replicate Your Microscopy Data?” *Journal of Cell Science* 134
(6): jcs254144. <https://doi.org/10.1242/jcs.254144>.

</div>

<div id="ref-jambor2021" class="csl-entry">

Jambor, Helena, Alberto Antonietti, Bradly Alicea, Tracy L. Audisio,
Susann Auer, Vivek Bhardwaj, Steven J. Burgess, et al. 2021. “Creating
Clear and Informative Image-Based Figures for Scientific Publications.”
*PLOS Biology* 19 (3): e3001161.
<https://doi.org/10.1371/journal.pbio.3001161>.

</div>

<div id="ref-karoune2022" class="csl-entry">

Karoune, Emma, and Esther Plomp. 2022. “Removing Barriers to
Reproducible Research in Archaeology.” *Zenodo, ver. 5 peer-reviewed and
recommended by Peer Community in Archaeology*, November.
<https://doi.org/10.5281/zenodo.7320029>.

</div>

<div id="ref-marqués2020" class="csl-entry">

Marqués, Guillermo, Thomas Pengo, and Mark A Sanders. 2020. “Imaging
Methods Are Vastly Underreported in Biomedical Research.” Edited by
Peter Rodgers and Elisabeth M Bik. *eLife* 9 (August): e55133.
<https://doi.org/ghmkv4>.

</div>

<div id="ref-marwicketal2018" class="csl-entry">

Marwick, Ben, Carl Boettiger, and Lincoln Mullen. 2018. “Packaging Data
Analytical Work Reproducibly Using R (and Friends).” *The American
Statistician* 72 (1): 80–88. <https://doi.org/gdhvm8>.

</div>

<div id="ref-marwickpilaar2018" class="csl-entry">

Marwick, Ben, and Suzanne E. Pilaar Birch. 2018. “A Standard for the
Scholarly Citation of Archaeological Data as an Incentive to Data
Sharing.” *Advances in Archaeological Practice* 6 (2): 125–43.
<https://doi.org/gf5vpk>.

</div>

<div id="ref-monterollopisQUAREPBareMinimal2025" class="csl-entry">

Montero Llopis, Paula, Chloë van Oostende-Triplet, Luis Acevedo, Sergiy
Avilov, Cristina Bertocchi, Ulrike Boehm, Lisa Cameron, et al. 2025.
“QUAREP - Bare Minimal Microscopy Reporting Requirements Checklist.”
*Zenodo*, March. <https://doi.org/10.5281/zenodo.14977578>.

</div>

<div id="ref-pawley2006" class="csl-entry">

Pawley, James B. 2006. “Points, Pixels, and Gray Levels: Digitizing
Image Data.” In, edited by James B. Pawley, 59–79. Boston, MA: Springer
US. <https://doi.org/10.1007/978-0-387-45524-2_4>.

</div>

<div id="ref-pedergnana2020" class="csl-entry">

Pedergnana, Antonella. 2020. ““All That Glitters Is Not Gold”:
Evaluating the Nature of the Relationship Between Archeological Residues
and Stone Tool Function.” *Journal of Paleolithic Archaeology* 3 (3):
225–54. <https://doi.org/grmgj2>.

</div>

<div id="ref-ryan2021" class="csl-entry">

Ryan, Joel, Thomas Pengo, Alex Rigano, Paula Montero Llopis, Michelle S.
Itano, Lisa A. Cameron, Guillermo Marqués, Caterina
Strambio-De-Castillia, Mark A. Sanders, and Claire M. Brown. 2021.
“MethodsJ2: A Software Tool to Capture Metadata and Generate
Comprehensive Microscopy Methods Text.” *Nature Methods* 18 (12):
1414–16. <https://doi.org/10.1038/s41592-021-01290-5>.

</div>

<div id="ref-samuel2020" class="csl-entry">

Samuel, Gabrielle, and Federica Lucivero. 2020. “Responsible Open
Science: Moving Towards an Ethics of Environmental Sustainability.”
*Publications* 8 (4): 54. <https://doi.org/grmgjx>.

</div>

<div id="ref-sarkans2021" class="csl-entry">

Sarkans, Ugis, Wah Chiu, Lucy Collinson, Michele C. Darrow, Jan
Ellenberg, David Grunwald, Jean-Karim Hériché, et al. 2021. “REMBI:
Recommended Metadata for Biological Imagesenabling Reuse of Microscopy
Data in Biology.” *Nature Methods* 18 (12): 1418–22.
<https://doi.org/10.1038/s41592-021-01166-8>.

</div>

<div id="ref-schmied2021" class="csl-entry">

Schmied, Christopher, and Helena Klara Jambor. 2021. “Effective Image
Visualization for Publications a Workflow Using Open Access Tools and
Concepts.” *F1000Research* 9 (February): 1373.
<https://doi.org/10.12688/f1000research.27140.2>.

</div>

<div id="ref-schmied2023" class="csl-entry">

Schmied, Christopher, Michael S. Nelson, Sergiy Avilov, Gert-Jan Bakker,
Cristina Bertocchi, Johanna Bischof, Ulrike Boehm, et al. 2023.
“Community-Developed Checklists for Publishing Images and Image
Analyses.” *Nature Methods*, September, 1–12.
<https://doi.org/10.1038/s41592-023-01987-9>.

</div>

<div id="ref-soler2022" class="csl-entry">

Soler, Santiago. 2022. “Cc-Licenses: Creative Commons Licenses for
GitHub Projects.” <https://github.com/santisoler/cc-licenses>.

</div>

<div id="ref-stark2018" class="csl-entry">

Stark, Philip B. 2018. “Before Reproducibility Must Come
Preproducibility.” *Nature* 557 (7707): 613–13.
<https://doi.org/gdh9xc>.

</div>

</div>
