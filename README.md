# A walkthrough to submit papers on arXiv

This is a quick guide to submit papers on [arXiv](https://arxiv.org). 

## Prerequisites and preliminary information

* The walkthrough is meant to guide you up to the point where the paper is ready for
  submission on arXiv, but **please do not not finalise the submission of this
  template, as this action is irreversible**. As you will see, a submission can not be
  triggered accidentally, so you are safe to experiment with the steps below. You
  should just avoid completing the submission, after the last step of the
  walkfthrough.

* The walkthrough assumes you have prior basic knowledge of how LaTeX works. It is
  also assumed you have created an account on [arXiv](https://arxiv.org). 

## Preparing a folder for submission

* From the right-hand side panel of our GitHub webpage, download the latest release of this
  repository. The Manuscript folder contains an example of LaTeX manuscript,
  including all the compilation files. 

* Create an empty `arxiv/` folder, at the same level as `Manuscript`. You will now
    start transferring files to this new folder: the main idea is to prepare a
    standalone folder that arXiv will compile, and recreate a pdf of your manuscript.
    There are some specific steps for arXiv submissions, tho

* Copy the manuscript source file (`.tex`) to the `arxiv/` folder. The main file must
    be at the top level of this folder (you can not put it in a subfolder).

* Copy your figures. In our example, this means copying `Manuscript/Figures` into
    `arxiv/Figures`, because our manuscript searches for figure files in this folder.
    ArXiv uses `pdflatex` for compilation, so we recommend using use a format compatbile with
    this compiler (`.pdf/.png/.jpg/`).

* Copy style and macro files to `arxiv/`. In the example, we are using the SIAM class and style
  files (`.cls` and `.bst` files), as well a file with personal macros (`.sty` file).

* Copy your bibliographic data. **If you use `bibtex`, as in this example, this step
  is a bit more delicate.** On our computer, we would compile a `.bib` file, and use
  `bibtex` in between several `pdflatex` compilations, to generate the
  bibliography. On our computer, the bibliographic data after compilation is stored
  in a `.bbl` file. ArXiv, does not run `bibtex` for the compilation. Rather, arXiv
  expects to find a fully compiled `.bbl` file in the main directory. Hence, you
  must copy the `.bbl` file resulting from your compilation to the `arxiv/` folder.

* Optionally, create and write a new `arxiv/00README.XXX` file. In this file, you can specify
  options to be passed to arXiv. In most of my submissions, this file contains just
  one word, namely `nostamp`. I use this to avoid that arXiv stamps the left-edge of
  the manuscript. More infos about the `00README.XX` file can be found
  [here](https://info.arxiv.org/help/00README.html)

* It is possible that your manuscript has a more complex structure than the one
  outlined above, and you may have to include additional files for your compilation.
  [This page](https://info.arxiv.org/help/submit_tex.html) may be useful. If you use
  Overleaf, refer to [their help documentation](https://www.overleaf.com/learn/how-to/LaTeX_checklist_for_arXiv_submissions)
  regarding how to prepare your document for submission to arXiv.

* When you are done, compress the `arxiv/` folder, for instance by creating the file `arxiv.zip`

## Upload your manuscript on arXiv

* Log in to Arxiv and click `START NEW SUBMISSION`

* Tick the appropriate boxes in the sections `Verify your Contact information`,
  `Submission Agreement`, and `Authorship`.

* Select a License for your document. As of the time of writing [NWO
  recommends](https://www.nwo.nl/sites/nwo/files/media-files/NWO%20Open%20Access%20policy%202016-2020_ENG_0.pdf)
  (but does not strictly require) to use any Creative Commons (CC) licence for your
  publication. **As a simple rule of thumb, uploading the accepted version of your
  manuscript on arXiv under the `CC BY: Creative Commons Attibution` license** makes
  it fuly compliant with NWO Open Science policy. Any variant of the CC BY licence is
  also compliant with the NWO Open Science policy. Clicking on the info `i` button on
  the Arxiv website will give a quick description of the license variant. 

* Specify a Subject class for the manuscript, and click `continue`.

* Upload the `arxiv.zip` file prepared in the last section. ArXiv will unpack the
  file, and provide you with a list of files. Click `Continue: Process Files`

* If the compilation has been successful, you can now preview your manuscript and
    click `Continue`. There is also a logfile that can help if something goes wrong
    in the compilation. [Here](https://info.arxiv.org/help/faq/mistakes.html) are
    common mistakes that cause the compilation to fail.

* Write Title, Author, and Abstract of the paper. The journal reference of your
  article, as well as its DOI, can be added at a later stage, if you don't have them
  yet. Press `Save and Continue`
  
* You are now at the final page of your submission. This is where this tutorial ends.
    In an ordinary publication, you can now preview the article and then submit,
    following the instruction under `View PDF`. **Please do not submit this
    template as this action is not reversible**.
