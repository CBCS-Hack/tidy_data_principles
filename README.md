# Tidy code, reproducible science with R

# Description

This is where I detail which piece of work (e.g. journal article) this repository is associated with, including a link to the article. I usually explain the structure of the repository below this.

This repository forms the basis of the workshop on tidy and reproducible code for R.

The ReadMe is an important file in any repository but regularly gets neglected. This is where you can tell would-be users of your code how your repository works, how they need to use it to make your work reproducible, where any additional large data is stored that is not suitable for github (very common).

There is so much info online about tips for [a good ReadMe file](https://www.freecodecamp.org/news/how-to-write-a-good-readme-file/) so develop your own best practices.

This particular repository steps us through a few key tips for creating more open and reproducible science. It is important to remember, there is no set way of doing things in R or any other programming language. What I go through here is the conventions I use, and you may find other, better ways of doing things for you. People tackle similar problems in a multitude of different ways in programming and scientific investigation. So lean into that.

There are, however, a number of basic principles that I (and other far more capable programmers) advocate for to improve the reproducibility of the science we do:

-   ***Utilise your READme file*** - makes everything so much clearer

-   ***Use projects*** - R projects are necessary to interface with Github and standardises your working directory to the location of the main project folder. If there are reasons you want to import or save outside of the R project - that is totally doable by specifiying file paths.

-   ***Keep scripts byte-size (😉)*** - avoid putting a whole analysis into one script with 320 bajillion lines of code. It is horrible to work through for you and others, and very easy to make mistakes. Break up large analyses into bite-size chunks.

-   ***Order scripts logically*** - so users know how to step through your methodology.

-   ***Give your repository a structure*** - separate folders for figures, data, and even scripts if you want to work that way (there are advantages to using scripts inside the main project folder too). Subfolders within those folders can be useful too. A messy repository is a confusing repository.

-   ***Use RMarkdown/Quarto documents*** - for documenting the process that is being run through with your code or even constructing your manuscript.

-   ***Aim to keep large data outside of the project*** - you may often need large datasets for your analysis. If storage space was infinite, we would ideally keep this in every repository we needed this large dataset in. But storage space is rarely infinite - Github has a limit of 100MB. So if you can, store large data that you need to tidy and reduce in size outside the project. If you need a synthesised or smaller subset of the data, import the raw dataset into the project in a tidying script and create new and tidy input files. Then add your tidying script to your gitignore file. If the data needs to be kept as it is but accessed through the analysis repeatedly then I typically have a large dataset folder that I tell git to ignore in transfers to Github, or I store the data directly into an open access repository. You can either pull the data down from the online repository - or you can store the whole folder in the repository for individual download.

-   \*\*\* Use Github issues to discuss and document project decisions \*\*\*

Much of this thinking is borrowed and combined from friends and colleagues I have learned from along my journey - notably people at the [National Center for Ecological Analysis and Synthesis](https://www.nceas.ucsb.edu/) and [OpenScapes](https://www.openscapes.org/) - and also amazing work by [Allison Horst](https://allisonhorst.com/). In particular see this fantastic resource from Julie Lowndes et al for [Supercharging your research](https://www.nature.com/articles/d41586-019-03335-4).

I go through these principles in the scripts contained in this project. And I outline how I usually present the contents of a respository in a READme.

# scripts

Most scripts for this project are located in the main project folder. But one is found in the scripts folder to demonstrate how you can store your scripts effectively in different locations. I usually have all my separate scripts in the scripts folder and then one master script that runs them sequentially.

| Script                            | Description                                                                                                                                                                                                                                                                                                                 |
|:----------------------|:-----------------------------------------------|
| 1_setting_up.Rmd                  | This script has two functions. The first is to collect resources to get readers using git, github and ssh keys. The second is demonstrate that R markdowns can be used purely to leave notes without even using code. They are working documents with multiple purposes.                                                    |
| 2_using_rmarkdown_quarto_docs.Rmd | How to walk readers through your code and methodology in a logical and easy to read fashion using Rmarkdown documents. The new generation of Rmarkdown is Quarto so I would encourage you to install it and give Quarto documents a go. These tools are so much more user-friendly than a busy and poorly labelled R script |
| 3_organise_your_data              | Demonstrates how, rather than having data files scattered everywhere, we can create multiple folders for files at different stages of processing within your analysis - see "Data" heading below. The same applies to figures.                                                                                              |
| scripts/4_using_here().Rmd        | Explanation of how to use the here() function in the 'here' package to efficiently create file paths when scripts are stored away from the main project folder.                                                                                                                                                             |

# data

|   folder   |                                                                                                              Description                                                                                                               |
|:--------------------------:|:------------------------------------------:|
|   input    |                               This folder holds the raw data needed for the analysis. Really large data is typically stored outside of the project and I have a script dedicated purely to tidying data                                |
|   int\_    |                                                 This is where processesed data that is not the final product (often you need intermediary data) before being used later down the line                                                  |
|   output   |                                                                                            Data products from the analysis are stored here                                                                                             |
| large_data | This is a folder that is usually not available through Github because storage is at a premium (max 100MB files) but I may have one of these to store large data in that I can later share exactly as it is through another online repo |

# figures

All analysis figures are stored here. Often I create subfolders within this for 'supplementary' which are useful for the supplementary information in a journal article or 'explore' for just being able to rapidly visualise data without it cuttering your main figures.

# docs

Important documents pertinent to this analysis and repository are kept in the documents folder - this could even be the manuscript for the analysis (particularly if you use Rmarkdown/ Quarto to write it).
