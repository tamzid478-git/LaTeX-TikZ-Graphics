Binary Tree Diagram using TikZ

This LaTeX code uses the TikZ package to draw a Binary Tree. The diagram illustrates a hierarchical structure where each node may have up to two children. One node is highlighted to represent the current or active node during an algorithm.

Code Breakdown

1. Required Package

\usepackage{tikz}

The tikz package provides the tools needed to draw the tree.

⸻

2. Tree Layout

level distance=1.5cm,
level 1/.style={sibling distance=4cm},
level 2/.style={sibling distance=2cm},
level 3/.style={sibling distance=1cm},

These settings control the appearance of the tree.

* level distance specifies the vertical distance between levels.
* sibling distance controls the horizontal spacing between nodes on each level.
* Different levels use different spacing to keep the tree balanced and readable.

⸻

3. Node Styles

normal/.style={...},
active/.style={...}

Two reusable styles are defined.

* normal creates the standard orange circular nodes.
* active creates a highlighted blue node to emphasize a particular node in the tree.

Using styles avoids repeating the same formatting for every node.

⸻

4. Building the Tree

\node ... 
child { ... }
child { ... };

The tree begins with the root node.

Each child command creates a new branch connected to its parent, allowing the entire binary tree to be constructed recursively.

⸻

5. Labels

label=above:1

Each node has an index displayed above it.

For the highlighted node,

label=left:$i$

adds the variable i to indicate the current node being processed.

⸻

6. Missing Child

child[missing]

This command reserves space for a child that does not exist.

It keeps the overall tree structure aligned, ensuring that the remaining nodes stay in their correct positions.

⸻

Output

The final diagram contains:

* A binary tree with multiple levels.
* Circular nodes containing numeric values.
* Index labels displayed above each node.
* One highlighted node representing the active or current node.
* A balanced layout maintained using child[missing].

This example demonstrates how TikZ can efficiently create clean and well-organized binary tree diagrams for data structures and algorithm visualizations.
