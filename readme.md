# CaSE  Coding final

Written for JHU's EN.560.291 course.

## description

This app:

1. imports the latest data from [HealthData.gov](https://healthdata.gov) and the [Johns Hopkins Center for Systems Science and Engineering](https://systems.jhu.edu/)
2. wrangles and geocodes the data
3. generates maps and textual summaries from the data
4. defines an interactive [Shiny](https://www.rstudio.com/products/shiny/) dashboard
5. handles user input to switch maps and summaries on-the-fly

All data wrangling and view generation happens in [`global.r`](global.r). Using these results, the Shiny app is then defined in [`ui.r`](ui.r) and [`server.r`](server.r). Finally, the app is styled as detailed in [`styles.scss`](styles.scss), taking inspiration from Statistics Sweden's [Kommuner i siffror](https://kommunsiffror.scb.se/)  (*Municipalities in Numbers*) visualization.

## usage

### online

Access the app online on [Shinyapps](https://solanto.shinyapps.io/case-coding-final/).

### local

To run the app locally, you'll need to have an [R interpreter](https://www.r-project.org/) installed. As well, to build dependencies, you will need [Rtools](https://cran.r-project.org/bin/windows/Rtools/).

Through an R shell, install the project's dependencies.

```R
install.packages(c("shiny", "magrittr", "dplyr", "leaflet", "formattable", "sass", "remotes"))
library(remotes)
install_github("hrbrmstr/albersusa")
```

Clone the repository and run the following in an R shell whose working directory is the repository's root directory:

```R
runApp()
```

Alternatively, open the project in RStudio and run the app using the IDE's built-in Shiny capabilities.
