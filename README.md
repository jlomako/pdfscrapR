# pdfscrapR
A bot written in R that extracts a table from a pdf file, processes the data and saves everything to a csv file. It runs every day around noon local time. It is a bit slow and has been replaced by a faster bot that does exactly the same thing but in python: <a href = "https://github.com/jlomako/pdfscraper">pdfscraper</a>


### note to myself about some problems I ran into:
* loading R package "pdftools" resulted in errors -->
 <a href="https://github.com/r-lib/actions/issues/78#issuecomment-611733294">solution</a>: use runner "macos-10.15" and install XQuartz before pdftools is installed: Add <code>run: brew install xquartz --cask</code> to yml file<br>
* GH stopped supporting macos-10.15 this summer (2022), runs on macos-11 now
* ggplot stopped working and has been de-activated until I find a solution
* created new yml file that loads packages from renv.lock (still runs on macos-11, ubuntu not working)
