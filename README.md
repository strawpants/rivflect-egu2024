# Latex Poster template for ITC UTwente style posters

modified by Roelof Rietbroek on April 2023 (adapted IGG Uni Bonn template)

This repository contains a set of latex files, a makefile script and some default logos needed to create a latex poster in A0 landscape or Portrait format.

## Prerequisites

* A working xelatex installation (in theory pdflatex would work as well buth no Arial fonts can then be used)
* A working bibtex installation
* The program Make (a Makefile is added for convenience)
* Installed [Carlito](https://fontlibrary.org/en/font/carlito) and Arial fonts



## Building a Poster in landscape format

### Clone the repository and modify the main file
You can change 'ConfPoster201xx' below to suit your needs.

    git clone https://gitlab.igg.uni-bonn.de/roelof/ITClatexposter.git Confposter20XX
    cd Confposter20xx/
    mv ITC_template.tex ConfPoster20xx.tex
and change in the [Makefile](Makefile): `` main1=ConfPoster20xx`` (without the .tex)

### Add new content boxes and tweak their positions 
The template has some example boxes which demonstrates you how new content can be added.
New plots and logos should be added to the folder [figures/](figures).
An [example bibtexfile](example.bib) is provided which can be renamed and modified if needed. 

### Run Make in the new folder
`make landscape`
or just 
    `make`
(and repeat until you get the positions of the boxes right)

## Building a Poster in Portrait format
Same as above but you run
    `make portrait`

## Use pdflatex instead of xelatex
This disables the Arial font for headers, but can be used if no Arial fonts can be installed on the system or if no xelatex is installed.
Just uncomment the line ``#latcom=pdflatex`` in the [Makefile](Makefile).






