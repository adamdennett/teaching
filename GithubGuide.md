Producing Reproducible Research Using RMarkdown and Github
================
Adam Dennett

In this practical session, you will learn how to produce work that is open, reproducible and portable using RStudio, RMarkdown, Git and Github.

-   [RStudio](https://www.rstudio.com/) is a graphical user interface (that you should already be familiar with) - it contains a number of features which make it excellent for authoring reproducible and open geographic data science work.

-   RMarkdown is a version of the [Markdown](https://en.wikipedia.org/wiki/Markdown) markup language which enables plain text to be formatted to contain links to data, code to run, text to explain what you a producing and metadata to tell your software what kinds of outputs to generate from your markdown code. For more information on RMarkdown, visit [here](https://rmarkdown.rstudio.com/lesson-1.html).

-   [Git](https://git-scm.com/) is a software version control system which allows you to keep track of the code you produce and the changes that you or others make to it.

-   [GitHub](https://github.com/) is an online repository that allows anyone to view the code you have produced (in whatever language you choose to program in) and use/scrutinise/contribute to/comment on it.

### Setting up GitHub to store your code

1.  If you are working on your own computer, you will first need to install git - <https://git-scm.com/> - if you are working on the UCL Remote Desktop, you won't need to do this as it is already installed for you.

2.  Go to <http://github.com> and install github (if working on your own computer). Create an account and create a new repository (call it anything you like - 'gis\_code' or something similar), making sure it is public and you check the box that says 'initialise new repository with a README' - click 'create repository' at the bottom

![Figure 1 - Setting Up Your Repo](images/git_repo_setup.png)

1.  Your new repository ('repo') will be created and this is where you will be able to store your code online. You will notice that a README.md markdown file has also been created. This can be edited to tell people what they are likely to find in this repository.

2.  Now you have created your repo online, you need to 'clone' it so that there is an identical copy of it in a local folder on your computer.

There are a couple of ways of doing this, but the easy one is to use the GUI that comes packaged with your git installation.

1.  The first thing you need to do is copy the Clone URL for your repo from the github website - click the green button in your repo for 'Clone or Download' and copy the link:

![Figure 2 - Getting Your Clone Link](images/copy_clone_link.png)

1.  Now in the windows start menu, go to git &gt; GUI

![Figure 3 - Git GUI 1](images/git_gui1.png)

1.  Select 'Clone Existing Repository' and paste the link from your GitHub account into the top box and the local directory that you want to create to store your repo in the bottom box (*note, you will need to add a name for a new folder, once you have selected an existing directory*).

![Figure 4 - Git GUI 2](images/git_gui2.png)

1.  After a few moments, you should now be able to view a copy of your GitHub repo on your local machine. This is where you will be able to store all of your code and some other files for your reproducible research.

### Using RStudio with git

Now, as I've mentioned before, RStudio is totally bad-ass. Not only does it make R fun to use, but the lovely people who created it also built in support for things like git!

For a full and excellent tutorial on using Git with R Studio, watch this webinar: <https://www.rstudio.com/resources/webinars/rstudio-essentials-webinar-series-managing-part-2/>

If you don't want to watch the vid, I'll do a quick summary below. So, to use git, first you need to enable it in RStudio:

1.  Open RStudio. In RStudio Tools &gt; Global Options, under 'Git/SVN' check the box to allow version control and locate the folder on your computer where the git.exe file is located. and Allow Version Control for new Projects and navigate to where the git.exe file is on your computer. Click OK.

![Figure 5 - Allow Version Control](images/rstudio_allow_version.png)

1.  Now in RStudio, you should create a new project in an existing directory - File &gt; New Project &gt; Existing directory - choose your new git repository as your new project folder. You may not need to restart RStudio.

#### Saving your work to your local cloned repo

1.  Open a new R Notebook in RStudio: File &gt; New File R Notebook

2.  Type some stuff (anything so that's it's not a blank empty file) at the top of the file and save it.

3.  As well as saving, which saves a copy to our local directory, we will also 'commit' or create a save point for our work on git. To do this, you should click the 'git' icon and up will pop a menu like the one below:

![Figure 6a - Git Integration with RStudio 1](images/git_rstudio.png)

You can also click the Git tab that will have appeared in the top-right window of RStudio

![Figure 6b - Git Integration with RStudio 2](images/git_rstudio.png)

1.  To Commit (save) the changes in this file to your local cloned git repository, first click 'Commit'

2.  Up will then pop another window that looks a little like the one below:

![Figure 7 - Reviewing Changes](images/rstudio_review_changes.png)

1.  In this window, you will be able to review the differences between any previous saves you have made to your document and the current changes. If you are happy with the changes, you can then select the file and click 'commit' to save them to your current local repo. If you are not happy, then you can always revert back to a previous version that you know did work!

2.  If I were you, I would save R Scripts or RMarkdown Documents using the usual save button quite regularly, and then every time you, then you can commit your changes then.

#### Pushing your changes to GitHub

1.  Once you are happy with your progress, you should also then 'Push' your changes to your online GitHub repo. This is important, both for backing up your work, but also for keeping a reproducable record of your research.

2.  To do this, first make sure you have committed any changes to your local cloned repo and then click the 'Push' button to whizz your code up to your master GitHub repo - you will probably be prompted to enter your github username and password to enable this...

![Figure 8 - Pushing to GitHub](images/git_push_pw.png)

#### Possible git problems

1.  There are many many possible git problems. As you continute to commit and push work, especially when using different clones, you may well run into things like merge conflicts and a whole load of other problems. I've just been trying to fix a merge conflict for the last hour and eventually got there. It's not easy. It's not pretty, but as ever, there is usually a guide somewhere on the internet to help you.

For merge conflicts, try here: <https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/>

For general github help, try here: <https://help.github.com/>

Reproducible Research Using R Markdown
--------------------------------------

OK, so now you have set everything up so that you can become a reproducable research ninja! All that remains is to do some reproducable research!

For the definitive guide on R Markdown, please read [R Markdown: The Definitive Guide](https://bookdown.org/yihui/rmarkdown/) - obviously! It will tell you everything you need to know, far beyond what I am telling you here.

There is also an excellent guide on the R Studio website -<https://rmarkdown.rstudio.com/lesson-1.html>

And a quick cheatsheet here: <https://github.com/rstudio/cheatsheets/raw/master/rmarkdown-2.0.pdf>

And an older one here: <http://www.rstudio.com/wp-content/uploads/2016/03/rmarkdown-cheatsheet-2.0.pdf>

One of the awesome things about R Markdown is it can be converted into a range of different formats - html for webpages, word documents, PDFs, blogs, books - virtually everything!

Now, earlier on in this exercise, I got you to open a new R Notebook or R Markdown file. They are both R Markdown Documents, but the Notebook allows chunks of code to be run independently.

1.  Go back to the notebook you created earlier in step 11. We are now going to insert some code from the practical last week and run it.

2.  In RStudio, you can either select Code &gt; Insert Chunk or you can Click the 'Insert' button and insert an R Chunk

![Figure 8 - Insert R Chunk](images/Insert_code_chunk.png)

1.  A box will appear and in this box, you will be able to enter and run your R code. Try pasting in:

``` r
library(tidyverse)
```

    ## Warning: package 'tidyverse' was built under R version 3.4.4

    ## -- Attaching packages ----------------------------------- tidyverse 1.2.1 --

    ## v ggplot2 3.0.0     v purrr   0.2.4
    ## v tibble  1.4.2     v dplyr   0.7.4
    ## v tidyr   0.8.0     v stringr 1.2.0
    ## v readr   1.1.1     v forcats 0.2.0

    ## Warning: package 'ggplot2' was built under R version 3.4.4

    ## Warning: package 'tibble' was built under R version 3.4.4

    ## Warning: package 'tidyr' was built under R version 3.4.4

    ## Warning: package 'purrr' was built under R version 3.4.4

    ## Warning: package 'dplyr' was built under R version 3.4.3

    ## -- Conflicts -------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
library(geojsonio)
```

    ## Warning: package 'geojsonio' was built under R version 3.4.2

    ## 
    ## Attaching package: 'geojsonio'

    ## The following object is masked from 'package:base':
    ## 
    ##     pretty

``` r
library(sf)
```

    ## Warning: package 'sf' was built under R version 3.4.4

    ## Linking to GEOS 3.6.1, GDAL 2.2.3, proj.4 4.9.3

``` r
library(tmap)
```

    ## Warning: package 'tmap' was built under R version 3.4.4

``` r
library(tmaptools)
```

    ## Warning: package 'tmaptools' was built under R version 3.4.4

``` r
#read some data attributes
LondonData <- read_csv("https://files.datapress.com/london/dataset/ward-profiles-and-atlas/2015-09-24T14:21:24/ward-profiles-excel-version.csv", na = "n/a")
```

    ## Parsed with column specification:
    ## cols(
    ##   .default = col_double(),
    ##   `Ward name` = col_character(),
    ##   `Old code` = col_character(),
    ##   `New code` = col_character()
    ## )

    ## See spec(...) for full column specifications.

``` r
#read some geometries
EW <- geojson_read("http://geoportal.statistics.gov.uk/datasets/8edafbe3276d4b56aec60991cbddda50_2.geojson", what = "sp")
#pull out London
LondonMap <- EW[grep("^E09",EW@data$lad15cd),]
#convert to a simple features object
LondonMapSF <- st_as_sf(LondonMap)
#append the data to the geometries
LondonMapSF <- append_data(LondonMapSF,LondonData, key.shp = "lad15cd", key.data = "New code", ignore.duplicates = TRUE)
```

    ## Data contains duplicated keys: E09000001

    ## Over coverage: 626 out of 659 data records were not appended. Run over_coverage() to get the corresponding data row numbers and key values.

``` r
#plot a choropleth
qtm(LondonMapSF, fill = "% Not Born in UK - 2011")
```

![](GithubGuide_files/figure-markdown_github-ascii_identifiers/unnamed-chunk-1-1.png)

1.  When including code chunks in your work, there are various options that allow you to do things like include the code, but not run it: display the output but not the code, hide warnings etc. Most of these can be input automatically by clicking the cog icon in the top-right of the chunk.

![Figure 9 - Chunk Options](images/chunk_options.png)

1.  Various other options and tips can be found in the full R Markdown guide on RStudio here: <https://rmarkdown.rstudio.com/lesson-1.html> and in this the cheatsheets linked to above.

Adding References to Your Work
------------------------------

Now, as you build up your documentation for the work you are doing, it is likely that you will want to include references to support your arguments.

Building a bibliography in your R Markdown document is quite simple, you will just need to install some additional packages that plug into RStudio and learn how to export your bibliography from your reference management software.

### Exporting a bibliography from Zotero

Here I will assume that you are going to be using Zotero as your reference management software. If you use other software, there are probably similar options for exporting available to you, so don't worry.

The aim is to get a list of references that are stored in a format known as `BibTeX` - <http://www.bibtex.org/>

I won't go into BibTeX now, but if you go on to write your dissertation using [LaTeX](https://www.latex-project.org/), then BibTeX is the format that you will use to store your references.

1.  Having built up a bibliograpy of relevant literature in zotero, you should export it in BibTeX format and save it to the same directory that your R Markdown project is located in. Go to File &gt; Export Library and select BibTeX as your format.

![Figure 10 - Zotero Export](images/zotero_export.png)

1.  Once saved into the same directory as your Markdown project (your

2.  Once your BibTex file is saved into the same directory as your, you can then tell your markdown document where to find the in the YAML text at the very top of your file:

``` r
---
title: "Producing Reproducible Research Using RMarkdown and Github"
output:
  html_notebook: default
  word_document: default
  
author: Adam Dennett
bibliography: 
 - RReferences.bib
  
---
```
