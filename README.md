Graph Implementation in JavaScript
This project contains a basic implementation of a Graph data structure in JavaScript. The Graph class uses an adjacency list to represent the graph, where each node is a key in an object, and its value is an array of its connected nodes (edges).

What is a Graph?
A graph is a data structure used to represent relationships between objects. It consists of:

Nodes (also called vertices): The objects or entities in the graph.
Edges: The connections between the nodes.
Graphs can be classified into:

Directed Graphs: Edges have a direction (e.g., node A -> node B).
Undirected Graphs: Edges do not have a direction (e.g., node A <-> node B).
Weighted Graphs: Edges have weights or values.
Unweighted Graphs: Edges do not have weights.
In this implementation, we focus on an unweighted, directed graph.

Features of the Graph Class
This implementation allows for:

Adding nodes: You can add nodes (vertices) to the graph.
Adding edges: You can add connections (edges) between the nodes.
Class Overview
Constructor
javascript
Copy
Edit
constructor() {
  this.nodes = {};
}
The nodes property is an object that serves as an adjacency list. Each key represents a node, and its value is an array of connected nodes.

addNode(node)
javascript
Copy
Edit
addNode(node) {
  if (!this.nodes[node]) {
    this.nodes[node] = [];
  }
}
Adds a node to the graph. If the node already exists, no changes are made.

addEdge(node, edgeNode)
javascript
Copy
Edit
addEdge(node, edgeNode) {
  if (this.nodes[node]) {
    this.nodes[node].push(edgeNode);
  }
}
Adds a directed edge from node to edgeNode. If node does not exist in the graph, no edge is added.

Example Usage
Here's an example of how to use the Graph class:

javascript
Copy
Edit
const graph = new Graph();

// Add nodes
graph.addNode("A");
graph.addNode("B");
graph.addNode("C");

// Add edges
graph.addEdge("A", "B");
graph.addEdge("A", "C");
graph.addEdge("B", "C");

// Adjacency list
console.log(graph.nodes);
// Output:
// {
//   A: ["B", "C"],
//   B: ["C"],
//   C: []
// }
Advantages of Using an Adjacency List
Efficient for Sparse Graphs: Uses less memory compared to adjacency matrices for graphs with fewer edges.
Easy Traversals: Great for traversing neighbors of a node.
Potential Enhancements
Add support for undirected edges.
Implement methods to remove nodes or edges.
Add a method to check if two nodes are connected.
Extend the graph to support weighted edges.
This is a basic explanation of graphs and how to use your Graph class. Let me know if you'd like any edits or additional details!
