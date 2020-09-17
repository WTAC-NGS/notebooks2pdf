# Style guide for Jupyter training notebooks
This document contains some guidelines for creating a new Jupyter training notbook so that is is compatible wth the notebooks2pdf script. 

* Put all notebook files for a tutorial in a single directory, and not in subdirectories.
* For figures, make a subdirectory called "img" or similar and put all images there.
* Below are some general guidelines for the layout of the new notebook:
  - With the exception of scripts, put commands in separate boxes, not together.
  - When using minus signs for equations, make sure to use the real minus sign and not the hyphen.
  - Make sure images are in their own box, and refer to them as:
  
   `![title](path/from/notebookdir)`

  - Give the image a short but decsriptive title, as this will show up in the pdf.
