Assignment 4 
Overview:
In the original lecture code, graphs used a separate Edge class to represent connections. This assignment restructures the graph model so that each Vertex directly contains its own outgoing edges using a map of neighbors and weights. This allows BFS and Dijkstra to be implemented in a more object-oriented way, where all relationships are encapsulated within the Vertex objects themselves.

The new structure still allows the unchanged Main.java from GitHub to run as expected.

Project Structure:
- Vertex.java
- WeightedGraph.java
- Search.java
- BreadthFirstSearch.java
- DijkstraSearch.java
- Main.java

Design Details:
1. Vertex uses a string id as identifier and stores a map of outgoing neighbors with weights.
2. Edge weights are stored as double values.
3. WeightedGraph handles all vertex and edge creation.
4. BFS is implemented using a queue and visited set.
5. Dijkstra uses Java’s PriorityQueue and a record class for queue entries.
6. The Search interface provides a unified API for both algorithms.

Build and Run Instructions:
Compile:
    javac -d out src/*.java

Run:
    java -cp out Main
