# tidy_data_principles

This repository forms the basis of the workshop on tidy and reproducible code for R.

The ReadMe is an important file in the repository but regularly gets neglected. This is where you can tell would-be users of your code how your repository works, how they need to use it to make your work reproducible, where any additional large data is stored that is not suitable for github (very common).

# scripts

Most scripts for this project are located in the main project folder with this ReadMe. But one is found in the scripts folder to demonstrate how you can store your scripts effectively in different locations.

| Script                            | Description                                                                                                                                                                                                                                                                                                                 |
|:-----------------|:-----------------------------------------------------|
| 1_setting_up.Rmd                  | This script has two functions. The first is to collect resources to get readers using git, github and ssh keys. The second is demonstrate that R markdowns can be used purely to leave notes without even using code. They are working documents with multiple purposes.                                                    |
| 2_using_rmarkdown_quarto_docs.Rmd | How to walk readers through your code and methodology in a logical and easy to read fashion using Rmarkdown documents. The new generation of Rmarkdown is Quarto so I would encourage you to install it and give Quarto documents a go. These tools are so much more user-friendly than a busy and poorly labelled R script |
| 3_organise_your_data              | Demonstrates how, rather than having data files scattered everywhere, we can create multiple folders for files at different stages of processing within your analysis - see "Data" heading below. The same applies to figures.                                                                                              |
| scripts/4_using_here().Rmd        | Explanation of how to use the here() function in the 'here' package to efficiently create file paths when scripts are stored away from the main project folder.                                                                                                                                                                 |

# data

| folder | Description |
|:------:|:-----------:|
| input | This folder holds the raw data needed for the analysis. Really large data is typically stored outside of the project and I have a script dedicated purely to tidying data |
| int_ | This is where processesed data that is not the final product (often you need intermediary data) before being used later down the line |
| output | Data products from the analysis are stored here |

# figures

All analysis figures are stored here. Often I create subfolders within this for 'supplementary' which are useful for the supplementary information in a journal article or 'explore' for just being able to rapidly visualise data without it cuttering your main figures.

# docs
Important documents pertinent to this analysis and repository are kept in the documents folder - this could even be the manuscript for the analysis (particularly if you use Rmarkdown/ Quarto to write it).


