# notebooks2pdf

[![Build Status](https://travis-ci.org/ngs-training/notebooks2pdf.svg?branch=master)](https://travis-ci.org/ngs-training/notebooks2pdf)   
[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-brightgreen.svg)](https://github.com/ngs-training/notebooks2pdf/blob/master/LICENSE)

This directory contains a number of scripts that can be used to convert Jupyter Notebooks to PDF. To increase sucess that this script will sucessfully convert the notebook to pdf please make sure that it conforms to the style guide in `styleguide.md`.

## Dependencies
- [MacTeX](https://tug.org/mactex/), texlive or similar
- pandoc
- anything listed in .travis.yml

## Usage
Make sure that your version of MacTeX (in particular lualatex) is up to date.  

In the notebook directory that you wish to convert, run:

`/path/to/make_course_pdf.py --no_exec <outprefix> <infile1, infile2, ...>`

Edit the .tex that was generated so that it looks ok (for instance by adding page breaks, checking that text wrapping in command blocks don't exceed page width, and fixing image positions).

If you want to add the keyboard icon to the boxes containing the prompt/commands, replace '\llap{{\color{#2}\[#3\]' with '\llap{{\color{black}\LARGE\faKeyboardO' in the .tex file.

Run lualatex to convert the .tex file to PDF.

`lualatex outputprefix.tex` 

Run lualatex again to ensure your PDF has a table of contents.

## Hints
* If an image wraps over a new page, it can cause blank spaces and unusual formatting. To get around it, put a /newpage line in the .tex file before the image.
* If you get errors about \faKeyboardO, make sure your version of mactex/texlive is up to date (for travis, this meant running tests in xenial).
