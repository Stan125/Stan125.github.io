---
layout: post
title:  "GREA: The RStudio Add-In to read ALL the data into R!"
date:   2016-07-17 18:00:00
categories: [R, RStudio]
---

[![GREA](https://github.com/Stan125/GREA/raw/master/images/logo.png)](https://github.com/Stan125/GREA/raw/master/images/logo.png)

Have you also been overburdened by the vast selection of R packages to read different filetypes into R? Do you sometimes just want to get that .csv file up and running in your environment, but forgot about all those endless `read.table()` options?

Well, GREA’s got you covered. [Gotta Read ‘Em All](https://github.com/Stan125/GREA) is an RStudio Add-In meant to help the R-User parse all important filetypes into R without having to remember any actual code or package. This is done interactively via a user interface built upon the [Shiny](http://shiny.rstudio.com) framework. For reading the files, <a href="https://cran.r-project.org/web/packages/rio/index.html">rio</a> (by Thomas Leeper) is used, which can read a vast amount of different filetypes.

Here's how it works: In the beginning, the user selects a file on his computer. After some adjustments (which are done interactively), the proper function to read the file is pasted into the console, with an object name that can be specified by the user. In between, the user can always head to the preview to see what the parsed file would look like with the current options.

### Installation

Installation is easy. Just run the following code:

```r
devtools::install_github("Stan125/GREA")
```

### Usage

#### 1. Starting the Add-In

Calling the Add-In is simple: just click on the Add-In Tab and select 'Gotta Read Em All'. The Add-In itself quickly pops up and you are ready to start!

#### 2. Selecting the Dataset

Once the Add-In is started up, press the "Select File" button to select a file on your computer. Then, type in a name for your desired dataset. Once the file is loaded into the Add-In, you may see additional options for parsing the file on the right. Ignore those for now and head right to the "previews" tab.

<p align="center">
<img src="https://github.com/Stan125/GREA/raw/master/images/step2.png" width="400" height="300" />
<p>

#### 3. Looking at the preview

The previews tab shows a preview of what your dataframe would look like if you parsed it with the current settings. If something looks odd (e.g. your column names fell into the first row of the dataset), head back to the first tab. We can see that in our case, the column and decimal separators are wrongly specified. If everything is right, still head back to the first tab. 

<p align="center">
<img src="https://github.com/Stan125/GREA/raw/master/images/step1.png" width="400" height="297" />
<p>

#### 4. Adjusting stuff

If the preview of your dataframe looked off, you now have the chance to adjust some parameters (e.g. Sheet Index for Excel files, or separator for .csv files). Adjust them so your preview looks exactly like you want them to. When you have typed in a name for your newly aquired dataset and are then finished, press "done". Afterwards, the function to read your dataset is pasted into your console. Boom! You're good to go.

<p align="center">
<img src="https://github.com/Stan125/GREA/raw/master/images/step3.png" width="550" height="97" />
<p>

### Remarks

RStudio Add-Ins require the newest release of RStudio. GREA can be found on this <a href="https://github.com/Stan125/GREA">GitHub Page</a>. Feedback and Suggestions are always very much welcome.
