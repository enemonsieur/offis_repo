---
Brain Connectivity: 
alias:  (ID questions/Blocks) (Summarize/Answer) (Revise 1-2-3) (Mindmap) 
---

Local efficiency
	Clustering surrounding a certain nodes
Clustering coefficient?
	prevalence of certain edges of the neighbours of the NODE compare to possible edges of the neighbour of the nodes. 
	This means are the bacteria cells connected to the maximum number of bacterias cells possible? Like the skin or is it more like a streptocok?
Betweenness centrality?
	It's like, take a node, take the shortest paths in the modules that passes through. For all the shortest paths inthe network, how much of them passes thourgh this MOFO node?
What's Degree?
	The degree of that shit is the number of links connected to the node. The more links a node has, the hgiher the degree. Is like Social Currency, the more friends, the cooler you are
What's a Hub?
	A MOFO Node that's like a celebrity (high degree)
Global efficiency?
	
How often a certain pattern appear in a network
	Is a triangle pattern appears often? Pyramidal? pentagonal---
	Each of the patterns has a meaning and we have to udnerstand them (p28)
Wha the fuck is modularity?
	It's when a network has a lot of edges connected with closed cluster, but not that much between away clusters
What's a path length?
	The number of edges connecting two networks
# Benchmark Networks
What the fuck is that?
	A method to generate some networks that have specific properties
	And we compare that to the networks we measured in fMRI 
	and we see if they match. (How much they match)
How many types of Networkds do you know?
	Regular, Small work NW, Modular...
What's the important NW our prof focused on?
	Small world Nw
## Small World Network
What the hell is a SWNW (small world network)
	A network with high Clustering coeff (each node has lots edges), but the path length (reaching far nodes) is almost equal to random(lot of shortcuts to all nodes

What's the diff beween a regular and a randomn network
	Regular: Lot of clusters, hard to reach far away nodes
	Random: Almost no clusters, as easy to reach far away nodes than close nodes


SCALE FREE NETWORK
How are they define?
	They have a central node with a looot of edges and then less and less nodes with high degree. 
	
What is p? #unclear
		The prob that we find cutted edges
How is this p diff in regular and random?
		The lower the p, the more regular (a lot of edges in the circle)
		the higher the p, the more the p in the inside

The brain is neither a randomnor a regular Nw. Nor a heterogenious distributed network. Which means the degree distribution is quite middle and the majority of brain nodes have only few links. 
Why do evolution favor SWNw?
	To optimise cost effective information processing. 
	If and edge cost axons etcc.. to create, we want less of them, and very clusters. But on the other hand, we wanna be able to go between brain regions without moving a lot so we need a bit of direct paths that connect ways paths

## Scale-free Networks
def
	The dgree distribution follows a power law p.36
	![[Pasted image 20220720144722.png]]
Like one or two nodes arevery connected, but the other one, really aren'T

Exemple: Streets connected to others: Few airports have many many links, and a lot of local airports with small links

How can we grow Scale free networks?
	You use prferential attachement
	You start with one node, and add more and more edges to each - The richer get richers
Why do we care bout that shit?
	Bc it may be how Nw develop overtime...

## Empirical Network
## How are brain maps analyzed
- we subdivide brains in different parcels
- Then compute the time series in ONe parcel (how the HDr changes in time?)
- Use a correlation map to get a node by node correlation matrix. 
	- Apply a threshold. Bigger than that is consider an actual, true edge between that nodes (obviously the correlation node1-tonode1 will always get the max threshold)
	- The more you increase that shit (threshold), the fewer edges you find)
	- For different threshold, you get different Corr matrix, and you can 
	- Why do we used timeseries?
		- To know that at different timeseries, the same B-regions/nodes are activated, so the correlation with those shits will be higher, the more they are correlated throughout the time-serie
	- 

What are the types of connectiviy?
	Strucutral: actually connect two brain areas. There's a goddamn physical link
	Functional: Only stat. depencies, Some sith is happening at the same time, But we don't know if they are connected
	Effective: Wait. But is there something affecting both of the connected areas? Is one influencing the other?