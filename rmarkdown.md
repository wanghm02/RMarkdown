Assignment R Markdown and Leaflet
================
Harry Wang
Jan 25, 2017

Including Code
--------------

The R code to show the schools in Hamilton city:

``` r
library(htmlwidgets)
library(leaflet)
hamiltonuniversity<-data.frame(lat=c(43.2620,43.2580,43.2383),
                               lng=c(-79.9203,-79.9060,-79.8861))


schoolnames<-c("McMaster University",
                 "Columbia International College",
                 "Mohawk College")

my_map<-        hamiltonuniversity %>%
        leaflet()  %>%
        addTiles() %>%
        addMarkers(popup=schoolnames)
my_map
```
