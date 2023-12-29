# Optimizing-Tourist-Itineraries-Using-Simulated-Annealing
In this project, I have used a stochastic optimization algorithm called Simulated Annealing to optimize tourist itineraries. I have used Python & Folium to generate resulting plots. 

## Problem Statement & Background

For a given set of tourist attractions, I plan to provide a quick and optimal travel itinerary based on user preferences. <br>
<br>
In an age where tourism is not just a leisure activity but a pursuit of cultural and personal
enrichment, the complexity of planning the perfect travel itinerary remains a universal
concern for travelers worldwide. Tourists often grapple with the complexities of optimizing their travel plans, attempting to strike a
delicate balance between maximizing exploration and minimizing logistical hurdles. This project aims to introduce an effective solution and serve as a valuable tool for tourists exploring
a new country or anyone seeking assistance in crafting personalized and efficient travel itineraries.

On a high level, this problem is a variant of the Traveling Salesman Problem (TSP). We know
that TSP is an NP-hard problem, meaning that as the number of cities increases, the number of
possible solutions grows exponentially, making it computationally infeasible to solve for large
instances using brute-force or dynamic programming algorithms such as the Held-Karp algorithm. For
instance, to find an optimal solution using brute force for N places there are (N - 1)! / 2 possible routes. Let’s say, if we want to compute for 20 places, there are ***60,822,550,204,080,000*** different possible routes. 

## Simulated Annealing

In such large search spaces, simulated annealing (a heuristic-based optimization algorithm) could be very
useful in finding a reasonably good solution within a limited time. This algorithm is inspired by the metallurgical practice of
annealing, where metals are heated to a high temperature and then gradually cooled. This controlled
process allows metal atoms to rearrange themselves into a more stable crystalline structure, thus
reducing defects and achieving a lower-energy state. Similarly, simulated annealing in optimization
allows for a deliberate and probabilistic exploration of the solution space, which helps in finding a
globally optimal solution by avoiding being trapped in local optima.
You can find the demo of the dashboard at this [YouTube Link](https://www.youtube.com/watch?v=ouDgxJT0jHE) <br>
<br>

<p align="center">
  <img src="https://github.com/thota-sasanth/Optimizing-Tourist-Itineraries-Using-Simulated-Annealing/blob/main/SA.png" width="300" height="250"> <img src="https://github.com/thota-sasanth/Optimizing-Tourist-Itineraries-Using-Simulated-Annealing/blob/main/SA.png" width="300" height="250">
</p>

<br>

## Data Preparation / Processing
I used two datasets taken from Kaggle. 

* US Census Demographic Data
* US Accidents Data (2016 - 2021)

The US census demographic data is generated/downloaded from **American Community Survey**, a
demographics survey program conducted by the U.S. Census Bureau. 
This other dataset is a country wide accident dataset, which covers 49 states and 3000 counties of the USA. The
accident data are collected from February 2016 to Dec 2021, using multiple APIs that
provide streaming traffic incident (or event) data. 

The above data has **2.8M+** accidents records. I applied different data processing techniques such as - data reduction, filtering only specific year data, null rows imputation, duplicates handling, columns standardization/encoding, plots for outlier detection and removal, feature extraction, merging two datasets, and clustering data using Kmeans algorithm.



## Dashboard Implementation & Components
I implemented the dashboard as in a client-server architecture. The dashboard consist of advanced charts - 

* Zoomable Choropleth Map
* Accident Severity Slider
* Parallel Coordinates Plot
* TreeMap
* Stacked Bar Chart
* Time Series Area Chart
* Radial Bar Plot

Every chart is linked with every other chart with wide range of **interactions**, **overlays**, **pop-ups**, and **brushings**. This way the user can easily get a deeper level of details and gain better insights.
<br>

## Findings
As the dataset taken is very large, there are a lot of insights that can be gathered after playing around with the dashboard. Some of the major findings I came across using the intearctions and dashboard are - 

* **Population has a high impact on accident rate**
* **Weekdays have most number of accidents compared against weekends**
* **8AM and 5PM are the peak times for accidents within a day**
* **Juntion, Traffic Signal, and Crossings are the top 3 accidents prone POI (point of interest) areas**
* **High humidity in the early mornings leads to more number of accidents**
* **Counties with most accidents have higher office job population compared to service job population**

You can gather a lot more insights leveraging this custom-designed visual analytics dashboard.
<br>
<br>
