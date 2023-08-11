# A walkthrough to submit papers on arXiv

This is a quick guide to submit papers on [arXiv](https://arxiv.org). 

## Prerequisites and preliminary information

* The walkthrough is meant to guide you up to the point where the paper is ready for
  submission, but **it is important that you do not finalize the submission of this
  template, as this is irreversible**. As you will see, a submission can not be
  triggered accidentally, so there is nothing to worry about. You should just avoid
  doing the final step

* We assume prior elementary knowledge of how LaTeX works.

* It is assumed that you have created an account on [arXiv](https://arxiv.org). 

## Preparing a folder for submission

* From the right-hand side panel of this, download the latest release of this
  repository. The Manuscript folder contains an example of LaTeX manuscript,
  including all the compilation files. 

* Create an empty `arxiv/` folder, at the same level as `Manuscript`. You will now
    start transferring files to this new folder: the main idea is to prepare a
    standalone folder that arXiv will compile, and recreate a pdf of your manuscript. 

* Copy the manuscript source file (`.tex`) to the `arxiv/` folder. The main file must
    be at the top level of this folder (you can not put it in a subfolder).

* Copy your figures. In our example, this means copying `Manuscript/Figures` into
    `arxiv/Figures`, because our manuscript searches for figure files in this folder.
    ArXiv uses `pdflatex` for compilation, so you should use a format compatbile with
    this compiler (`.pdf/.png/.jpg/`).

* Copy style and macro files to `arxiv/`. In the example, we are using SIAM class and style
  files (`.cls` and `.bst` files), as well a file with personal macros (`.sty` file).

* Copy your bibliographic data. **This step is a bit more delicate.** On our
  computer, we would compile a `.bib` file, and use `bibtex` in between several
  `pdflatex` compilations, to o generate the bibliography. On our computer, the
  bibliographic data after compilation is stored in a `.bbl` file. ArXiv, does not
  run `bibtex` for the compilation. Rather, arXiv expects to find a fully compiled
  `.bbl` file in the directory. Hence, you must copy your `.bbl` file to the `arxiv/`
  folder.

* Optionally, create and write a new `arxiv/00README.XXX` file. In this file, you can specify
  options to be passed to arXiv. In most of my submissions, this file contains just
  one word, namely `nostamp`. I use this to avoid that Arxiv stamps the left-edge of
  the manuscript. More infos about the `00README.XX` file can be read
  [here](https://info.arxiv.org/help/00README.html)

* It is possible that your manuscript has a more complex structure than the one
  outlined above, and you may have to include additional files for your compilation.
  [This page](https://info.arxiv.org/help/submit_tex.html) may be useful. If you use
  Overleaf, refer to [their help documentation](https://www.overleaf.com/learn/how-to/LaTeX_checklist_for_arXiv_submissions)
  regarding how to prepare your document for submission to arXiv.

* When you are done, compress the `arxiv/` folder, for instance by creating the file `arxiv.zip`

## 
