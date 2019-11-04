---
layout: exercise
topic: Loops
title: Multi-file Analysis
language: R
---

You have a satellite collars on a number of different individuals and want to be able to quickly look at all of their recent movements at once.
The data is posted daily to a url as a zip file that contains one csv file for each individual.
Start your solution by:

* Downloading the zip file using `download.file`
* Unziping it using `unzip`
* Obtaining a list of all of the files with file names matching the pattern `"collar-data-.*.txt"`

1. Use a loop to load each of these files into R and make a line plot (using `geom_line`) for each file with `long` on the `x` axis and `lat` on the `y` axis.
Graphs, like other types of output, won't display inside a loop unless you explicitly display them, so you need to either put your `ggplot` command inside a `print` statement. Include the name of the file in the graph as the graph title using `labs`.

2. Add code to the loop to load each of these files into R, calculate the minimum and maximum latitude in the file, and store these values, along with the name of the file, in a data frame.
When you create the empty data frame you'll need to include `stringsAsFactors = FALSE` to prevent the `character` column for the file name becoming a `factor`.
Show the data frame as output.