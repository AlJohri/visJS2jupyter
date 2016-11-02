# visJS2jupyter
visJS2jupyter is a tool to bring the interactivity of networks created with vis.js into jupyter notebook cells, authored by members of the UCSD Center for Computational Biology & Bioinformatics (http://compbio.ucsd.edu)
--------------

Authors: Brin Rosenthal (sbrosenthal@ucsd.edu), Mikayla Webster (m1webste@ucsd.edu), Aaron Gary (agary@ucsd.edu), Julia Len (jlen@ucsd.edu)

A simple use example is included in the notebooks folder.  In the example provided, we show how to display a graph created with NetworkX using visJS2jupyter.  Here the networks displayed within Jupyter notebook cells may be dragged, clicked, and hovered on, and zooming is enabled within the window.  Nodes and edges may be styled with properties available from vis.js networks (see http://visjs.org/docs/network/ for a list and description of properties).  The main function is 'visjs_network', which requires two inputs which describe the nodes and edges in the network- 'nodes_dict', and edges_dict'.  The other arguments are optional, and apply general styles to the graph, such as sizes, highlight colors, and physics properties of the graph.

An interactive use example of visJS2jupyter may be found here: http://bl.ocks.org/brinrosenthal/raw/fd7d7277ce74c2b762d3a4d66326215c/ (scroll to the bottom to see the network).  In this example, we display the bipartite network composed of diseases in The Cancer Genome Atlas (http://cancergenome.nih.gov/), and the top 25 most common mutations in each disease.  We also overlay information about drugs which target those mutations.  Genes which have a drug targeting them are displayed with a bold black outline.  The user may hover over each gene to get a list of associated drugs.

Another module is 'visualizations', which contains the 'graph_union' function. This function takes in two graphs and displays their union. Intersecting nodes are triangles and non-intersecting nodes are either circles or squares, depending on which graph they belong to. An interactive example of visualizations may be found here: https://bl.ocks.org/julialen/raw/d21c9d378cb09b5a7181497101996727/. In this example, we graph the union of two networks of 100 nodes each. The user can hover over each node to see the graph it belongs to and the node name.

To install, run "pip install visJS2jupyter" in your terminal. To import the visJS_module, use the statement "import visJS2jupyter.visJS_module". To import the visualizations module, use the statement "import visJS2jupyter.visualizations".
