---
title: 'RStudio Tutorial: Stacked and Side-by-Side Bar Graphs'
date: '2019-03-27T21:36:10-05:00'
draft: false
---
This tutorial will go over how to create stacked and side-by-side bar charts in RStudio with ggplot.

To get started, make sure you have ggplot installed using

```r
install.packages("tidyverse")
```

`tidyverse` contains multiple different packages including ggplot.

Next, we'll import the data set and include `tidverse` like so:

```r
library("tidyverse")

# The path of the file will depend on your machine, make sure it's changed
# accordingly
movies = read.csv("D:/Intro to Stats/Movies_06-15txt.csv")
```

And make a basic bar graph:

```r
ggplot(movies, aes(x = MPAA)) + 
  geom_bar()
```

![null](/images/bargraph_1.png)

We can now display more variables my adding an additional argument to `aes()` in the `ggplot()` function. To display an additional variable, specify the `fill` argument making it equal to a name of a categorical variable in your data set.

```r
ggplot(movies, aes(x = MPAA, fill = Genre)) + 
  geom_bar()
```

![null](/images/bargraph_2.png)

By default, ggplot will display it as a stacked bar graph. To get the bars to display side-by-side, we'll add an argument to `geom_bar()`:

```r
ggplot(movies, aes(x = MPAA, fill = Genre)) + 
  geom_bar(position = "dodge")
```

![null](/images/bargraph_3.png)

By specifying the position argument, we can change the position of the individual bars. For "dodge", think of it as the bars are dodging each other to reach the x-axis of the graph.

Looking at your previous graphs, you can see that the "NC-17" rating is hard to see, and it looks like there are more than just Drama movies in the side-by-side graph. To fix this, we can display the bars as percentages rather than just counts. We can change the position argument:

```r
ggplot(movies, aes(x = MPAA, fill = Genre)) + 
  geom_bar(position = "fill")
```

![null](/images/bargraph_4.png)

By changing position equal to "fill", we can see that bars "fill" up their column. We can now see that NC-17 includes Horror films as well as Drama films. On the y-axis, you can see that the percentages are represented by decimals rather than percents. We can fix this by adding an additional function:

```r
ggplot(movies, aes(x = MPAA, fill = Genre)) + 
  geom_bar(position = "fill") + 
  # Change the y scale to percent
  scale_y_continuous(labels = scales::percent) + 
  # Change the y label
  ylab("Percent")
```

![null](/images/bargraph_5.png)
