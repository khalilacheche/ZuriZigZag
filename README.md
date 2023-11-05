# Story
Have you ever been delayed by public transportation, making you late for important appointments? It's a common inconvenience, and it's what inspired me to work on this project. In a fast-paced world, we rely on navigation systems to get us where we need to be on time. However, these systems often assume that every bus or train will run punctually, which isn't always the case. That's why we developed Zigzag, an innovative solution.

While Google Maps is a fantastic tool, it operates under the assumption that all public transportation will be on time, which, as we all know, isn't always true. This is particularly evident in Switzerland, where even the most efficient systems can face delays. That's where ZuriZigzags comes in.

# Our mission was clear:

To provide optimal routes based on real conditions.
To consider the historical performance of each transportation route.
To adapt to the variability and unpredictability of public transportation.
# What
Our project's primary goal was to enhance the accuracy and reliability of navigation in the context of public transportation. We wanted to move beyond the assumption that all buses and trains would run on schedule and provide users with routes that reflect the real conditions they may encounter.

# How
Our approach involved several key steps:

Step 1: Retrieving relevant stations: We created a weighted directed graph to represent Zurich's transportation network, with stops as nodes and connections as edges. This allowed us to identify relevant stations for the desired path, taking into account travel time between stops.

Step 2: Adding schedule constraint: We constructed a second graph from a subset of relevant nodes, where each node represented a connection between two stops at a specific time. Nodes were connected if it was feasible to transfer between them based on arrival and departure times. Shortest path calculations were then used to determine the optimal route.

Uncertainty and Delay: We addressed the issue of uncertainty when trains or buses are late. By applying the Central Limit Theorem and considering historical data, we approximated delays. The goal was to calculate the probability that a user would arrive at their desired time, accounting for these delays.

# Challenges
The project presented several challenges that needed to be addressed:

Data Preprocessing: Preparing the dataset for the model involved a significant amount of data cleaning and processing, ensuring that only relevant and reachable stops were considered.

Selection of Subset Nodes: The selection of subset nodes for path planning only considered travel time, which was an initial limitation.

No Parallelization: The path detection process lacked parallelization, which could be a potential area for improvement.

# Result
Our project aimed to enhance the accuracy of navigation under real-world public transportation conditions. By considering historical data, delays, and other real-world factors, we created an innovative solution that could adapt to the variability and unpredictability of public transportation. While the project had its limitations, such as walking distance calculations and data preprocessing, it represents a significant step toward improving public transportation navigation.