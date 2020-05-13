# Recruitment task

Hi! In this task, we would like you to show us that you can perform basic operations on reStructuredText (RST) files.

If you have never worked with the RST format before, see [reStructuredText Primer](https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html) for an introduction. In the ``doc`` folder of this repository, you will also find some documentation files that are written using RST. They should give you a good idea how to handle this format.

Note: RST files can be viewed and edited with any text editor, for example Notepad++.

Your task is to convert the small documentation section that you got from us in Word format (*Upgrade with nRF Connect for Mobile*) into RST, in such a way that it becomes an integral part of the documentation set that already exists in this repository.

## GitHub repository

This GitHub repository already contains some documentation files in the ``doc`` folder. You will find three types of files in there:

* RST files with ``.rst`` extension. They hold the content of this small documentation set. View them to see how RST syntax looks like. Your main task involves editing some of these files or adding new RST files (whichever you consider more appropriate).
* Images in the ``doc/images`` folder. These image files are referenced from RST and displayed in the HTML documentation. You will need to add some image files here as part of your task.
* All other files. They constitute the build framework that we have set up for you. They are used to build HTML from RST. Do not edit them in any way or things might stop working.

## Interacting with the repository files

GitHub allows you to view the files in this repo, but to interact with them in any way, you will need to get them onto your hard drive.
Follow this workflow to download and edit the files:

1. Use the Download button to get the zipped files onto your PC.
2. Unzip the downloaded repository.
3. Complete your task.
4. Zip the repository with your added/modified RST files and send it to us via email.

## Building the output

After downloading the repo to your PC, start by building HTML documentation output from the already existing RST files. You will find the build instructions in ``/doc/building_the_docs.rst``.

This will give you an idea of how different RST syntax is reflected in the resulting HTML.

When you are done with the task, it is also important that you check the result of your work by building HTML again, to see the output including the RST files that you have added or edited. Any build errors or warnings indicate that something is wrong in the RST syntax. Make sure that the added content displays correctly in the HTML output.

## Content to be added

*Upgrade with nRF Connect for Mobile* contains several mistakes of various sort. When converting this content to RST, try to find and correct as many as you can. For this task, you can rely solely on the information in this small documentation set and do not need to consult other documentation.

Additionally, think whether all the content from *Upgrade with nRF Connect for Mobile* should be kept in one chunk or whether it makes sense to divide it and put it in more than one RST file. Remember that you can either create new RST files in the ``doc`` folder or you can choose to only edit the existing ones.

## Task objective

Your task is successfully completed when we receive a zipped repository where the content from  *Upgrade with nRF Connect for Mobile* is part of the RST source files and of the resulting HTML output.
