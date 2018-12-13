# Student README file
Note: No changes were made to the pre-written methods `Display.java`, `Edge.java`, or `Vertex.java`
These are the methods I wrote

1.`computeAllEuclideanDistances()`
-
- this method goes through each vertex, and each ofits adjacent edges. then, for each edge on the graph,it computes the euclidian distance between the sourcevertex and the target vertex, using the distance formula. 

2.`computeEuclidianDistance()`
-
- Similar to computeAllEuclideanDistances(), this method converts coordinate points into Euclidean distances. The only difference here is that instead of looping through all vertices, this method takes the x and y coordinates of two specific vertices, and returns the Euclidean distance between them.

3.`leastWeight(LinkedList<Vertex> unknown)`
- 
- This is a helper method for `doDijkstra(String s)` it takes in the LinkedList of unknown vertices and returns the vertex with the minimum weight. 
To compute the minimum weight, we arbitrarily set the first element in unknown equal to min 
then we iterate through all unkown vertices. Every time a smaller one is found, it gets replaced as the min and we reset the associated min vertex to the vertex with that minimal distance. At the end of the loop, the vertex with the smallest distance will be set to minVertex and that will get returned.  


4.`doDijkstra(String s)`
-
- This method takes in a string to represent the starting city. We then use the getVertex(String s) method to get the vertex associated with the given city name. We can now carry out Dijkstra's algorithm using the logic in Weiss's pseudocode starting from this vertex. 

5.` getDijkstraPath(String s, String t)`
-
- This method is where we actually call doDijkstra. We call it on the starting point `String s`. Then we simply have to work backwards from t (the endpoint) and print its .prev field until we reach the point where .prev is null. We also make an edge for each step in the path that includes the Euclidean distance. At the very end, I copied the LinkedList into a new LinkedList called `copy` so that I could clear `path` (for future use) but still return the proper list at the end of the method.  
