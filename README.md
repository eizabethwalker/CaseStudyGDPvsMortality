# Case Study: Do higher-income countries experience lower death rates? What do we do about it from a public health perspective?

Socioeconomic standing could be a strong factor contributing to death rates. While testing for the global relationship may be more difficult due to confounding variables and complex interactions, I will try to determine the basic research question: “Does higher GDP per capita have a relationship with death rates? Then I will determine real-world applications of the results.

# Objective

Determine if GDP and Mortality Rates have a relationship. Determine real-world applications.

# Design Process

I used RStudio to clean and merge the data sets. I then created three graphs using RMarkdown.

## Step 1: Data Collection

The data for this project was retrieved from [OurWorldInData.org] (https://ourworldindata.org), and the unit of observation is country-year. The GDP data comes from [GDP per capita Worldbank] (https://ourworldindata.org/grapher/number-of-deaths-per-year), which has 7063 observations. The Death Rate Data comes from [Number of Deaths Per Year] (https://ourworldindata.org/grapher/gdp-per-capita-worldbank ) and produces 18944 observations. The two datasets were cleaned and merged, resulting in a reduction of observations to 6741. The final data set includes 203 different countries and 34 different years running from 1990 to 2023, though not every country appears in every year.

### Cleaning the Data

The data was cleaned by removing columns with invalid names and ensuring column names matched and were prepared for merging.

## Step 2: Density Plots

Both of the data sets were cleaned, so two density plots were created.

### Density Plot of GDP across Country-Years (1990-2023)

![image](https://github.com/user-attachments/assets/c2f14e6c-efb7-4df1-8e54-9d1bcab57723)

The above figure displays a density plot of GDP. As displayed, the range is wide, starting at zero and ending at 150000 with one mode in a positively skewed manner. The data suggests that a majority of countries lie above 5000 GDP in ‘low GDP.’

### Density Plot of Deaths across Country-Years(1990-2023)

![image](https://github.com/user-attachments/assets/83f1aa0b-7039-4764-b587-1dd7c9e4ed1c)

The second figure displays a density plot of deaths across country-year. The range exists from 0e+00 to 3e+05. The graph is positively skewed, with the mode generally around 5e+04.

## Step 3: Merging the Data

The data was then merged to the specifications of "entity", "code" and "year".

## Step 4: Relationship between GDP per Capita vs. Total Deaths

![image](https://github.com/user-attachments/assets/1fe17384-ac43-447b-8939-c734e219f936)

The blue line represents the conditional mean of Total Deaths given GDP per capita, effectively modeling the expected value of mortality as a function of income. The surrounding gray ribbon denotes the confidence interval around this estimate, reflecting the degree of statistical uncertainty associated with the mean prediction. The relatively narrow width of the ribbon across the GDP range indicates high precision in the estimate; however, the intervals widen at the extremes of the distribution, particularly at very low and high income levels, likely due to smaller sample sizes or higher variance in those regions.

For countries with a GDP per capita exceeding approx. $20,000, the estimated mean of Total Deaths remains consistently low, as indicated by the flat and near-zero trajectory of the blue line. This pattern suggests that higher-income countries, on average, experience fewer total deaths annually, potentially due to better healthcare infrastructure, higher life expectancy, or more robust public health systems. The limited fluctuation in this range implies low variability in mortality outcomes among wealthier nations.

In contrast, among countries with GDP per capita below $20,000, the data exhibit greater heterogeneity. The increased dispersion of individual observations (black dots) and the upward trend of the mean line indicate that lower-income countries are subject to substantially higher and more variable mortality levels. This may be attributable to structural vulnerabilities such as larger population sizes, inadequate healthcare access, or exposure to environmental and infectious disease risks. While the dataset appears to be sufficiently large and diverse to support generalizable inference under typical modeling assumptions, the definition of the reference population is not explicitly stated. It remains unclear whether the observations represent all countries in a single year, a time-averaged cross-section, or a panel of countries over multiple years.

## Summary

The data indicates a negative association between GDP per capita and mortality rates, with wealthier nations exhibiting significantly lower mean death counts. This relationship is not strictly linear, as the majority of the variation is concentrated in the lower-income segment. These findings suggest that economic development may be inversely related to population-level mortality, though the relationship is likely confounded by factors such as population size, demographic structure, and health system capacity. Future research should incorporate controls for these variables and consider longitudinal data to better isolate causal mechanisms and temporal dynamics

## Applications

Public health campaigns could focus on providing mobile health clinics, nutrition support programs, fortification, and clean water projects in areas with a lower GDP per capita.
