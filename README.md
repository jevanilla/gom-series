GOM-Series
================

``` r
source("setup.R")
```

    ## here() starts at /mnt/s1/projects/ecocast/projects/nrecord/gom-series

### Buoy data aggregated to monthly means

``` r
x <- read_buoy_met() |>
  dplyr::group_by(buoy)

ggplot(data = x, aes(x = month, y = wind_speed, color = buoy)) +
  geom_line()
```

![](README_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->
