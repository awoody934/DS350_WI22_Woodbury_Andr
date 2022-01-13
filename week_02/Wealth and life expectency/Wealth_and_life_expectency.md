---
title: "CASE STUDY TITLE"
author: "YOUR NAME"
date: "January 12, 2022"
output:
  html_document:  
    keep_md: true
    toc: true
    toc_float: true
    code_folding: hide
    fig_height: 6
    fig_width: 12
    fig_align: 'center'
---






```r
# Use this R-Chunk to import all your datasets!
```

## Background

_Place Task Background Here_

## Data Wrangling


```r
# Use this R-Chunk to clean & wrangle your data!
new_data <-filter(gapminder, gapminder$country != "Kuwait")
```

## Data Visualization


```r
# Use this R-Chunk to plot & visualize your data!

ggplot(data = new_data) + 
  geom_point(mapping = aes(x = lifeExp, y = gdpPercap, size = pop , color = continent ))+ 
  theme_bw()+
  scale_y_continuous(trans = "sqrt")+
  facet_wrap(~year, nrow = 1)
```

![](Wealth_and_life_expectency_files/figure-html/plot_data-1.png)<!-- -->

```r
ggsave("wealth_and_life_expectency.png")
```

## Conclusions
