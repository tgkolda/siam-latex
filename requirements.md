Goal is to modernize the SIAM LaTeX class and bibtex files, to support hyperlinking and supplemental materials, among other considerations.

Overall Requirments

* Must be able to generate PDF directly with pdflatex and postscript via latex and dvips. Hyperlinks must work in PDF generated via ps2pdf. 
* A single version should be usable for online and printing.
* PDF should not have any features
* Update bibliography to support DOI, URL or EPRINT.
* Include hyperlinking, include macros to support the hyperlinks.
* Integrated support for supplemental materials, include crossreferencing.
* "Review" mode, with line numbers and "for review" watermark.

Requirements for CLS

* Include hyperref package (needed for linking).
* Automatic bookmarks corresponding to section headings.
* Automatic completion of PDF fields such as title, authors, abstract, etc.
* Color hyperlinks with some options for visible (in the same way as for SIADS?) and invisible links.
* Create cross-referencing commands with hyperlinking: \secref (section), \tabref (table), \figref (figure), \algref (algorithm), etc. (Or maybe autoref or clever ref??) 
* Class option to specify supplemental file. Supplemental file has numbers starting with "S" (e.g., section, figure, table, algorithm, theorem, etc.). Pulls original title and authors from main document. 
* Class options to specify give a single sequence of numbers to the figures, tables, algorithms, equations, etc. (The old style uses the section number on the label number.)
* Class option to specify "for review" that adds link numbers and "for review only" watermark.

Requirements for BST

* Support for printing DOI, URL, and EPRINT, including hyperlinking.
* Support for arXiv and other preprint services.

Requirements for Instructions

* Create an example/userguide in one package, including bib file, external figures,  seperate supplemental latex file, etc.
* Show the code to generate the desired behavior in the PDF of the guide itself (i.e., don't need to look at source code).
* Example of new theorem-like environments, e.g., property, example, remark.
* Example of including EPS in PDFLATEX using eps2pdf package.
* Example of tikz for a plot with several lines.
* Example of using new hyper-referencing macros.
* Reference examples: Article with DOI, software with URL, web page, arXiv preprint, other preprint with URL.
* Example of referencing between supplement and main document, in both directions. In other words, example of citing a table in the supplement from the main document and also a theorem in the main document in the supplement.
* Care in inserting labels so that link is in the right place in the document (i.e., it's better to jump to the BOTTOM of a figure rather than its top.)

Experimental Ideas

/Maybe to be implemented via class options??/

* Make the spacing more generous, especially before and after theorem]like statements are around bulleted lists.
* Example of code listing (Matt Knepley).
* Backref (David Gleich) 
* Lower case title or support so that cut-and-paste works as we would wish (i.e., not all caps) (Tammy Kolda)
* Center each page (SISC editorial board meeting)
* microtype (David Gleich??)
* Include amssymb,amsfonts,amsmath in class file by default (Tammy Kolda)


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
