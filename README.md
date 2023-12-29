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

<br>

<p align="center">
  <img src="https://github.com/thota-sasanth/Optimizing-Tourist-Itineraries-Using-Simulated-Annealing/blob/main/SA_algorithm1.png" width="400" height="300"> <img src="https://github.com/thota-sasanth/Optimizing-Tourist-Itineraries-Using-Simulated-Annealing/blob/main/SA_1.png" width="400" height="300">
</p>

<br>

The algorithm starts at a high temperature with a random initial solution and gradually finds an optimal solution after cooling down based on a neighborhood exploration strategy. The model flow chart looks like - 
<br>
<br>
<p align="center">
  <img src="https://github.com/thota-sasanth/Optimizing-Tourist-Itineraries-Using-Simulated-Annealing/blob/main/SA_flowchart.png" width="450" height="700">
</p>

## Data 
I have curated a dataset of the Top 50 real-world tourist attractions, with precise
geographical coordinates and additional descriptions obtained from [latlong.net](https://www.latlong.net/country/united-states-236.html) <br>


## Experiments / Simulations
I worked on two different settings of the problem - Open and Closed versions of TSP. I conducted multiple experiments & simulation runs to find the best results for a given input. The dataset is shuffled & attractions are picked uniformly random as input for our model. The model parameters such as starting temperature, cooling factor, etc, are tuned. The best solution based on a pre-defined objective function (such as total travel distance, travel time, travel costs, weighted combinations) was stored. To ensure the reliability of the results, multiple replication runs were conducted with same order of attractions to reduce output variance. 


## Results
The below plots show the results for the best run for closed TSP scenario for 15 tourist attractions - 

<br>

<p align="center">
  <img src="https://github.com/thota-sasanth/Optimizing-Tourist-Itineraries-Using-Simulated-Annealing/blob/main/initial_sol.png" width="600" height="300"> 
  <img src="https://github.com/thota-sasanth/Optimizing-Tourist-Itineraries-Using-Simulated-Annealing/blob/main/SA_sol.png" width="600" height="300">
</p>

<br>

You can gather a lot more insights leveraging this custom-designed visual analytics dashboard.
<br>
<br>
