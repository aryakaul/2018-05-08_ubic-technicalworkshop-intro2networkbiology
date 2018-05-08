# Introduction to Network Biology

## 0. Set-Up
Please have the following packages/software installed prior to attending the workshop:

* Jupyter Notebooks
* Cytoscape
* networkx

## 1. Introduction to Cytoscape

1. Let's import a basic network into Cytoscape.  To do this, paste the network’s
[URL](http://www.ndexbio.org/#/network/2b2e62ef-392a-11e8-8695-0ac135e8bacf?accesskey=0c7ae1bef2ce580dd23584d532304fe6756ebc8aa2d86c121df8dca31a04cc2a) into the NDEx search widget in the Network Control Panel at the upper left of the Cytoscape window, and
then click on the Search icon.

2. Apply layouts and styles to visualize this network. Distinguish between proteins, small molecules, and RNAs. Also distinguish between directed and undirected edges. Use [Cytoscape's tutorial](https://cytoscape.github.io/cytoscape-tutorials/protocols/modules/mapping-data/#/) to learn how to do this. *Tip: Install yFiles layouts in the `Layout` tab*

3. Create an [NDEx](http://www.home.ndexbio.org/create-an-ndex-account/) account, and export your network to it. Go to `File->Export->Network to NDEx`. Click on the anonymous account in the upper right, then the Add Account button. Enter your NDEx username and password leaving the NDEx server field blank. 

## 2. Introduction to networkx and NDExBio

1. Use `pip` to install NDExBio
2. Open up a `Jupyter Notebook`
3. Use the following command to find the documentation for NDExBio.
```
help(NDEx)
```
4. Load the graph found at the following UUID: 6a19-586e-11e7-8f50-0ac135e8bacf
5. Convert the graph to a NetworkX object
6.Re-label the node names by using the relabel_nodes function. Hint: the node names are stored in your node attributes. You can access them using get_node_attributes function.
7. Instead of studying the entire network directly, we will use a seed and create a subnetwork from this seed node by collecting all of its first degree neighbors. We will continue to expand this subnetwork by collecting the neighbors of neighbors (and so on) until we reach a minimum of 1000 nodes. Write the necessary function that takes a graph, node, and the minimum number of nodes as input and returns the expanded subgraph. Use BRCA2 as the seed node. *Tip: you can get all direct neighbors using the neighbors() method.*
8. Display this network by using the draw function. Hint: Make sure matplotlib is imported and you are using the matplotlib inline Jupyter magic.
