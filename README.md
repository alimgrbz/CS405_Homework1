# CS 405 Homework 1: Suicide Statistics Visualization (2000-2022)

**Author**: Alım Gürbüz  

## Overview

This project visualizes data on the number of suicides and the crude suicide rate between 1975 and 2022. For the purpose of this assignment, the visualization focuses on the data from 2000 to 2022 using JavaScript.

## Data Description

The dataset is structured as follows:

- `year`: Represents the year of the data.
- `value`: The number of suicides for that year.
- `rate`: The crude suicide rate for that year.

## Visualization Details

The visualization is divided into two parts: Bars and Curve.

- **Bars**: Represents the number of suicides. 
  - Color: `steelblue`
  - Representation: Uses `<rect>` SVG elements.
  - Proportionality: Height is relative to the value it represents, with the max height determined by the dataset's max value.
  
- **Curve**: Represents the crude suicide rate per thousands.
  - Color: `red`
  - Representation: Uses `<path>` SVG elements. 
  - Proportionality: The height of each point on the curve is based on the rate for that year, with the peak determined by the dataset's max rate.

Additionally:

- The x-axis indicates the years.
- The y-axis displays values. Not every bar corresponds to a y-axis label. Instead, `yAxisLabelsCount` is set to 20 distinct y-axis divisions, and the `valueIncrement` is used to determine the numerical gap between these labels.
- Horizontal and vertical axis lines are drawn using the `<line>` SVG element.
  
Styling is enhanced using CSS to offer a clearer visual distinction. Styles are applied using CSS class selectors, affecting bars, curve, legends, label fonts, and stroke widths.

## Code Explanation

- The `<svg>` element houses the visualization.
- Dimensions are set using `svgWidth` and `svgHeight`.
- Individual bars are spaced with `barPadding`.
- Bar width is determined using `barWidth`.
- `maxValue` and `maxRate` retrieve the highest value and rate from the dataset.
- A margin object offers spacing for the SVG canvas.

## Visual Presentation


---<img width="659" alt="Screenshot 2023-10-18 143558" src="https://github.com/alimgrbz/CS405_Homework1/assets/134507100/6e700f52-d423-455e-9c42-f7377e4a1d52">


