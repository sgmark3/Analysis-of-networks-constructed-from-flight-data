# Flight Network Analysis & optimizing itineraries of fleet of aircrafts.
We extract flight networks from various open source data sources such as The Bureau of transportation and Statistics (US Bureau of transportation). By representing the network as graphs, we can study different salient features of the aviation transportation networks
traversed by specific airlines during a specific time window within certain country or continent. A preliminary analysis is performed 
in this jupyter notebook by computing centrality measures and shortest paths between two arbitrary locations. We can also do a clustering analysis by finding cliques of different sizes. Cliques are complete connected network motifs. For example, triangle is a clique with 
three nodes and a tetrahedron is a clique with four nodes. Using centrality measures we can predict the busy airports and depot locations
(HQ) of airlines. Note that we pick Southwest airlines (WN) for our analysis, but the user can change the airline by entering a different two letter code in the fifth cell of the notebook. 

We also compute a itenararies for 51 aircrafts that visit each and every node (airport) in the flight network exactly once. There are 72
airports (nodes) and 721 routes (edges) in the flight network. None of these tours involve visiting more than three airports including the depot.
We used the Google OR Tools for solving the VRP. The codebase with documentation and examples is available at the following website: 
https://developers.google.com/optimization/routing/vrp

The data that is used in the analysis is from the following website:
https://www.transportation.gov/policy/aviation-policy/domestic-airline-consumer-airfare-report

Some other sources of datasets on flights and commerical aviation:

1) A database on flights with over 10,000 airports worldwide: https://openflights.org/data.html#airline
2) This a repository of flight data hosted by OpenSky network. In there, the travel data before and during the COVID-19 pandemic from year 2019 to 2021 can be found: https://opensky-network.org/data/datasets#d4
3) A dataset on airline delays: https://www.kaggle.com/giovamata/airlinedelaycauses
4) A website to look up currently working flights worldwide: https://www.flightsfrom.com/
