Directed Graph (Digraph) using TikZ

This LaTeX code uses the TikZ package to draw a Directed Graph (Digraph). The graph consists of multiple vertices connected by directed edges, where each arrow represents the direction of a relationship between two vertices.

Code Breakdown

1. Required Library

\usetikzlibrary{arrows.meta}

The arrows.meta library provides modern arrowheads such as Stealth, which are used for the directed edges.

⸻

2. Defining the Vertex Style

vertex/.style={
circle,
draw=red!70!black,
fill=orange!15,
thick,
minimum size=8mm
}

A reusable style named vertex is defined.

Each vertex is displayed as:

* A circular node.
* A dark red border.
* A light orange fill.
* A thick outline.
* A fixed minimum size for consistent appearance.

Using a style avoids repeating the same formatting for every node.

⸻

3. Creating the Vertices

\foreach \v/\x/\y in { ... }

A \foreach loop creates all vertices automatically.

For each entry:

* \v is the vertex label.
* \x is the x-coordinate.
* \y is the y-coordinate.

This approach makes it easy to add, remove, or reposition vertices without rewriting multiple \node commands.

⸻

4. Drawing the Directed Edges

\foreach \a/\b in { ... }

Another \foreach loop creates all directed edges.

Each pair represents a connection from vertex \a to vertex \b.

For example,

m/q

draws a directed edge from m to q.

The command

\draw[->,thick] (\a)--(\b);

draws a thick line with an arrowhead, indicating the direction of the edge.

⸻

Output

The final diagram contains:

* Fourteen labeled vertices.
* Directed edges connecting related vertices.
* Consistent node styling using reusable TikZ styles.
* Arrowheads that clearly indicate edge direction.

This example demonstrates how TikZ and \foreach loops can efficiently generate clean and maintainable directed graph diagrams for graph theory, algorithms, and network visualizations.
