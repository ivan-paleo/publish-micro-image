
<!-- TOC ignore:true -->
# How to share data on Zenodo

By Ivan Calandra

<!-- TOC ignore:true -->
# Table of content

<!-- TOC -->

- [Introduction](#introduction)
- [Register at Zenodo](#register-at-zenodo)
- [Create a new upload](#create-a-new-upload)
    - [Community](#community)
    - [Files](#files)
    - [DOI](#doi)
    - [Other metadata](#other-metadata)
    - [Visibility](#visibility)
    - [Publish](#publish)
    - [Share](#share)
- [Edit an existing upload](#edit-an-existing-upload)
    - [Edit metadata](#edit-metadata)
    - [Edit data](#edit-data)
- [Share your GitHub repositories](#share-your-github-repositories)
    - [Connect GitHub with Zenodo](#connect-github-with-zenodo)
    - [Make your repository public](#make-your-repository-public)
    - [Create a new release](#create-a-new-release)
    - [Get a DOI automatically](#get-a-doi-automatically)

<!-- /TOC -->



# Introduction

This template explain the main steps to upload files to [Zenodo](https://zenodo.org/). The [help pages on the Zenodo website](https://help.zenodo.org/) explain most of it probably better, but I have found that what colleagues usually lack are clear step-by-step instructions.  
The first time using Zenodo can feel complicated, especially because it is often done as a last step before submitting a paper.  
Therefore, I hope these instructions will help make it easier to every user.

While most steps are very general, some points are specific to LEIZA's IMPALA and/or TraCEr lab. Adapt as necessary!

Also note that I present only Zenodo. Not because it is the only alternative or because it is better, but simply because this is the tool I have been using for some years now. I like it, it does what I need and I find it quite simple.  
But you might want to have a look at some alternatives, e.g. [OSF](https://osf.io/),  [Figshare](https://figshare.com/) or [Dryad](https://datadryad.org/stash).


# Register at Zenodo
An account is necessary so first [sign up](https://zenodo.org/signup/), or [sign in](https://zenodo.org/login/) if you already have an account.


# Create a new upload
The [help page](https://help.zenodo.org/docs/deposit/create-new-upload/) details the steps nicely so I will not repeat them here, but I will focus here on some extra considerations.

## Community
Please select the [*TraCEr-IMPALA_Monrepos-LEIZA*](https://zenodo.org/communities/tracer-monrepos/) community, so that all uploads related to either TraCEr or IMPALA can be linked.

## Files
It is not possible to upload folders, only files. So if the folder structure is important, ZIP the folders and upload them as if they were files. The drawback with this approach is that it will not be possible to download each file within the ZIP archive individually.

**You should always have a README to explain what the files are.** Make sure you tick the box *Preview* for the README file so that it will be the file displayed directly by default when someone opens the upload.

## DOI
Zenodo can reserve a DOI: under *Basic information > Digital object identifier*, if you specify that you do not have a DOI already, you get the option to *Get a DOI now!*  
When you do that, the DOI will be reserved, even before the upload is [published](#publish). That means that you can already use it e.g. in your manuscript or in files in the upload itself.

## Other metadata
1. Title: I recommend to use the title of the manuscript, appended with the type of data in the upload, as the title of the upload, e.g. "Title [microscope data]".
2. Creators/Contributors: Add all authors, either as *Creators* or *Contributors*.
3. License: an open license is necessary, but there are many. My favorite is "Creative Commons Attribution Share Alike 4.0 International" ([CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)) because it "forces" users of your data to share their data in open access as well.
4. Related works: in case this upload relates to other works, specify their identifiers here. Related works could be other uploads related to the same paper/project (e.g. different types of data), a published pre-print, a database (web interface)...

## Visibility
The visibility can be *Restricted* if you want to avoid people accessing your data before the paper is published. In that case, make sure you get a link for the reviewers and editors (see section [share](#share)).

**Latest when the paper is published, make sure that the visibility is set to *Public*.**

## Publish
Before publishing, you can *Preview* the upload to check that everything is fine.  
It is also possible to *Save draft*, especially in case you want to [reserve the DOI](#doi) but do not want to publish yet.

Before you click on *Publish*, it is important to understand that **the data (files) cannot be changed once the upload is published**, whether public or restricted, because a DOI links to specific data. Different data = different DOI. So be sure that you have a proper files uploaded before publishing.   
If you do need to change the files, refer to the section [Edit data](#edit-data).

## Share
If the upload is public, do not share it with its URL (https://zenodo.org/records/...) but rather with its DOI (https://doi.org/10.5281/zenodo...). To get the DOI, the easiest is to click on the DOI badge (in the *Details* section in the column on the right side) and copy/paste the *Target URL*.

**As long as the upload is restricted, share it with a link. This is the link that must be forwarded to the reviewers/editors.**  
Follow the instructions [here](https://help.zenodo.org/docs/share/link-sharing/).  



# Edit an existing upload
## Edit metadata

## Edit data


# Share your GitHub repositories
## Connect GitHub with Zenodo

## Make your repository public

## Create a new release

## Get a DOI automatically