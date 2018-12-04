# Group structures, clustering, and core-periphery analysis in venture capital co-investment networks
Venture capital firms often co-invest with each other on startup venture as part of syndicate investment teams. The ties formed by co-investing together influence the strategy and performance of the venture capital firms and the entrepreneurs they fund, and certain positions in this network are more beneficial than others. Thus, in this project, I analyze groups and clusters in the networks of venture capital co-investment, in order to see how the network changes over time and whether such social connections have impact on success of investments. 

Dataset contains deal information outcomes of funding event of venture capital firms from Jan 1981 to July 2014.

Some assumptions:
* Consider a relationship tie to exist between venture capital firms when the firms invest together in the same round of a portfolio company
* Consider firms as tied together if they invest together at least once, which means ignore multiple instances of a relationship
* Allow relationships to persist over time, so that the network in July 2014 is comprised of all cumulative ties that have occurred up to this point

## 1. Find the most central firm
First, I build the network for all the firms. Here I consider the most central firm to be the firm with the largest closeness centrality. The result shows that Intel Capital is the most central one. Besides, to verify the firm with the highest closeness centrality also has the lowest
average path distance, I calculate the average path distance for each node in network. The theory is verified by the result.
## 2. Analyze the development of network over time
Next, I look at the development of the network over time. Here I allow the network to be updated monthly for each month in the data, adding the new ties that occur through investments in the current month. Since coreness represents the highest-degree k-core to which a firm belongs, I plot the average “coreness” of the venture capital network over time. When a node is a member of a k-core with a high degree, its surrounding ties are very dense. When many nodes are members of k-cores with high degrees, this suggests that there may exist dense clusters within the network.
* Plot coreness allowing relationships to persist over time
* Plot coreness allowing ties to “decay”(Remove ties from the network if they are not renewed within 10 years)

The results show that two plots are very similar, which tells us that removing those relationships that were not renewed within 10 years doesn't affect the coreness situation of the entire network. It may indicate that core relationships in the network are usually long-lasting. 
## 3. Core-periphery analysis
When many nodes are members of k-cores with high degrees, this suggests that there may exist dense clusters within the network. According to that, I explore and find that recent network is more of a structure made up of core-periphery structure, instead of distinctly clustered components, with following two evidences.
* The number of nodes which have coreness more than average coreness of network,divided by total number of nodes, is decreasing over time.
* The median of coreness in the network is also decreasing over time.
## 4. Relationship between being in the core and firm's performance
In the end, I focus on whether being in the core of the network helps venture capital firms and the entrepreneurs they work with to perform better.  
* Relationship between closeness centrality and successful investments
* Relationship between closeness centrality and go-out-of business 

The results show that being in the core of the network does help the entrepreneurs that VC firms work with be less likely to go out of business. While the relationship between being in the core and successful investments is positive but not significant. 
