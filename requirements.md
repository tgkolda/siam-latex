Goal is to modernize the SIAM LaTeX class and bibtex files, to support hyperlinking and supplemental materials, among other considerations.

Overall Requirments

* Must be able to generate PDF directly with pdflatex and postscript via latex and dvips. Hyperlinks must work in PDF generated via ps2pdf.  - DONE
* A single version should be usable for online and printing. - DONE if "hidelinks" option is enabled
* PDF should not have any features - NOT SURE WHAT THIS MEANS?
* Update bibliography to support DOI, URL or EPRINT. - DONE
* Include hyperlinking, include macros to support the hyperlinks. - DONE
* Integrated support for supplemental materials, include crossreferencing. See http://www.sciencemag.org/content/345/6196/535/suppl/DC1 for a nice example with a coverpage on the front of the material, which may be nice to emulate. - DONE
* "Review" mode, with line numbers and "for review" watermark. - Partly DONE. Have line numbers, but no watermark.

Requirements for CLS

* Include hyperref package (needed for linking). - DONE
* Automatic bookmarks corresponding to section headings. - DONE
* Automatic completion of PDF fields such as title, authors, abstract, etc. - Not automatic, but included in examples.
* Color hyperlinks with some options for visible (in the same way as for SIADS?) and invisible links. - DONE
* Create cross-referencing commands with hyperlinking: \secref (section), \tabref (table), \figref (figure), \algref (algorithm), etc. (Or maybe autoref or clever ref??)  - DONE via cleveref
* Class option to specify supplemental file. Supplemental file has numbers starting with "S" (e.g., section, figure, table, algorithm, theorem, etc.). Pulls original title and authors from main document.  - DONE, but requires "shared" data to pull title and authors.
* Class options to specify give a single sequence of numbers to the figures, tables, algorithms, equations, etc. (The old style uses the section number on the label number.) - No option --- just done that way.
* Class option to specify "for review" that adds link numbers and "for review only" watermark. - Partly DONE. Adds line numbers but no watermark.

Requirements for BST

* Support for printing DOI, URL, and EPRINT, including hyperlinking. - DONE
* Support for arXiv and other preprint services. - DONE
* Support for referencing bibtex entries in original paper as well as possible additional references in the supplement, numbering should start with "S". (Maybe this is impossible, so we should instead just have separate references in the supplement.) - IMPOSSIBLE (or nearly so). Instead, require separate bibliographies.

Requirements for Instructions

* Create an example/userguide in one package, including bib file, external figures,  seperate supplemental latex file, etc. - DONE
* Show the code to generate the desired behavior in the PDF of the guide itself (i.e., don't need to look at source code). - DONE
* Example of new theorem-like environments, e.g., property, example, remark. - DONE
* Example of including EPS in PDFLATEX using eps2pdf package. - DONE
* Example of tikz for a plot with several lines. - DONE
* Example of using new hyper-referencing macros. - DONE
* Reference examples: Article with DOI, software with URL, web page, arXiv preprint, other preprint with URL. - DONE
* Example of referencing between supplement and main document, in both directions. In other words, example of citing a table in the supplement from the main document and also a theorem in the main document in the supplement. - DONE
* Care in inserting labels so that link is in the right place in the document (i.e., it's better to jump to the BOTTOM of a figure rather than its top.) - DONE previously.

Experimental Ideas

/Maybe to be implemented via class options??/

* Make the spacing more generous, especially before and after theorem]like statements are around bulleted lists. - DONE
* Example of code listing (Matt Knepley). - Have an algorithm, but not code.
* Backref (David Gleich) - Not done
* Lower case title or support so that cut-and-paste works as we would wish (i.e., not all caps) (Tammy Kolda) - Not done
* Center each page (SISC editorial board meeting)
* microtype (David Gleich??)
* Include amssymb,amsfonts,amsmath in class file by default (Tammy Kolda)
* Proof environment that works when the proofs ends in a math equation, or at least an example of how to hack it. (Tammy Kolda) - DONE

Software citation example to be incorporated:

@misc{clawpack,
    title={Clawpack software},
    author={Clawpack Development Team},
    url={http://www.clawpack.org},
    note={Version x.y}
    year={2013}}

will produce

C. D. Team, Clawpack software, …

(We need to fix this, by giving an example of how to correctly format the bibtex entry.)

DONE
