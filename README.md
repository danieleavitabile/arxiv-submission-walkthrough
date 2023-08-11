# A walkthrough to submit papers on arXiv

This is a quick guide to submit papers on [arXiv](https://arxiv.org). 

## Prerequisites and preliminary information

* The walkthrough is meant to guide you up to the point where the paper is ready for
  submission, but **it is important that you do not finalize the submission of this
  template, as this is irreversible**. As you will see, a submission can not be
  triggered accidentally, so there is nothing to worry about. You should just avoid
  doing the final step

* It is assumed that you have created an account on [arXiv](https://arxiv.org). 

## Preparing a folder for submission

* From the right-hand side panel of this, download the latest release of this
  repository. The Manuscript folder contains an example of LaTeX manuscript,
  including all the compilation files. 

* Create an empty `ArXiv/` folder, at the same level as `Manuscript`. You will now
    start transferring files to this new folder: the main idea is to prepare a
    standalone folder that arXiv will compile, and recreate a pdf of your manuscript. 

* Copy the manuscript source file (`.tex`) to the `ArXiv/` folder. The main file must
    be top level of this folder (you can not put it in a subfolder).

* Copy your figures. In our example, this means copying `Manuscript/Figures` into
    `ArXiv/Figures`. ArXiv uses `pdflatex` for compilation, so you should use a
    format compatbile with this compiler (`.pdf/.png/.jpeg/`).

* Copy your style and macro files to `ArXiv/`. In the example, we are using SIAM class and style
  files (`.cls` and `.bst` files), as well a file with personal macros (`.sty` file).


