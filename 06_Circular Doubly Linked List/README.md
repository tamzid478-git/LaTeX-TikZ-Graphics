Circular Doubly Linked List using TikZ

This LaTeX code uses the TikZ package to draw a Circular Doubly Linked List. The diagram contains a sentinel node (L.nil), multiple data nodes, bidirectional links between adjacent nodes, and circular connections that join the last node back to the sentinel.

Code Breakdown

1. Required Libraries

\usetikzlibrary{shapes.multipart,positioning,arrows.meta}

These libraries provide:

* shapes.multipart for creating nodes with multiple sections.
* positioning for placing nodes relative to one another.
* arrows.meta for modern arrow styles such as Stealth.

⸻

2. Defining Node Styles

normal/.style={...},
active/.style={...}

Two reusable styles are defined.

* normal creates the standard data nodes with a light yellow background.
* active creates the sentinel node with a cyan background to distinguish it from the data nodes.

Each node is divided into three horizontal parts, resembling the layout commonly used for linked-list nodes.

⸻

3. Creating the Sentinel Node

\node[active] (n0) {};

This creates the sentinel node.

Another node containing the label L.nil is placed to its left, and an arrow points to the sentinel to indicate the head of the linked list.

⸻

4. Creating the Data Nodes

\foreach \v ... in {25,9,36,16,4}

A \foreach loop automatically generates the five data nodes.

For each iteration:

* A new node is placed to the right of the previous node.
* The current value (25, 9, 36, 16, or 4) is inserted into the center section of the node.
* remember=\i as \p keeps track of the previously created node, eliminating the need for manual indexing.

⸻

5. Drawing Forward and Backward Links

\draw[->] ...

Two arrows are drawn between every pair of adjacent nodes.

* The upper arrow represents the next pointer.
* The lower arrow represents the previous pointer.

Small vertical shifts (yshift) keep the arrows from overlapping.

⸻

6. Creating the Circular Connections

\draw[->] ...

Two long arrows connect:

* the last node back to the sentinel node, and
* the sentinel node back to the last node.

These connections make the linked list circular, allowing traversal in both directions without reaching a null pointer.

⸻

Output

The final diagram contains:

* A sentinel node (L.nil).
* Five data nodes arranged horizontally.
* Bidirectional links between adjacent nodes.
* Circular links connecting the first and last nodes.
* Clearly separated node fields representing the structure of a doubly linked list.

This example demonstrates how TikZ can be used to create clean and reusable data structure diagrams for textbooks, lecture notes, and algorithm visualizations.
