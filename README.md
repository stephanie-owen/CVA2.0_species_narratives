# CVA2.0 Species Narratives

This repository contains supplementary information for the Climate Vulnerability Assessment 2.0.

The main product of this repository is a Quarto book of Species Narratives for each species included in the assessment. The Quarto book is rendered via Github Actions.

The template contains the following folders:

### .github

Contains a "workflows" folder. "publish.yml" sets up the Github Actions to run upon pushing to the "main" branch of this repo.

### bib_files

Houses the raw bibtex citations for each species. These are combined into "references.bib", which is then used in creation of the Quarto book.

### chapters

Contains a quarto script for each species, corresponding to individual species pages in the Quarto book. These scripts are created via "utils/child_doc.qmd", but should be edited manually if adding text or image paths.

### docs

-   'chapters' folder : contains html documents for each of the qmd files in 'chapters'. Produced by rendering the Quarto book in the terminal or through Github Actions.

### test_images

Currently houses placeholder images used for testing purposes. This folder should be renamed to "images" once the project is complete and house all related images that are included in the Species Narratives.

### utils

-   child_doc.qmd: Skeleton document to create individual species child documents. Text or images specific to each species should be made in "chapters/", not here.
-   child_doc.html: HTML format of the "child_doc.qmd" script
-   create_chapters.R: Script containing a function to create the child documents using "child_doc.qmd" as a template. This should not need to be re-run.
-   references.bib: Contains all references (in bibtex format) that are cited in each of the species narratives. If adding a citation, simply add the bibtex citation here and reference in the text by using the \[\@\] syntax.

In addition, this project contains the following files that are included in or needed to run the Quarto book:

### \_quarto.yml

YML for the Quarto book.

### index.qmd

File created with the Quarto project in Rstudio. This file may need to be updated or expanded to add information to the book when necessary.

### intro.qmd

File created with the Quarto project in Rstudio. This file may need to be updated or expanded to add information to the book when necessary (i.e., adding information about the CVA).

### references.qmd

Sets up full references page if desired. For references on individual pages, use "utils/references.bib".

### summary.qmd

File created with the Quarto project in Rstudio. This file may need to be updated or expanded to add information to the book when necessary.

#### Legal Disclaimer

This repository is a scientific product and is not official communication of the National Oceanic and Atmospheric Administration, or the United States Department of Commerce. All NOAA GitHub project code is provided on an ‘as is’ basis and the user assumes responsibility for its use. Any claims against the Department of Commerce or Department of Commerce bureaus stemming from the use of this GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.
