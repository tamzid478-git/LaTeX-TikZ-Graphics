Probability Tree Diagram Explanation

This LaTeX code uses the TikZ package to create a simple probability tree diagram. The tree illustrates two stages of events: Colour and State, with probabilities labeled on each branch.

Code Breakdown

1. Required Package

\usepackage{tikz}

Only the tikz package is required because the diagram consists of nodes and connecting lines.

⸻

2. Starting Point

\coordinate (S) at (0,0);

Defines the root of the probability tree. All branches originate from this coordinate.

⸻

3. Column Headings

\node at (3,6) {\Large\underline{\textbf{Colour}}};
\node at (7,6) {\Large\underline{\textbf{State}}};

These nodes create the two headings:

* Colour
* State

They organize the diagram into two levels.

⸻

4. Creating the Event Nodes

\node (W) at (3,2) {White};
\node (B) at (3,-2) {Black};
\node (WC) at (7,4) {Clean};
\node (WD) at (7,0) {Dirty};
\node (BC) at (7,-1) {Clean};
\node (BD) at (7,-5) {Dirty};

The first stage contains two possible colours:

* White
* Black

Each colour branches into two possible states:

* Clean
* Dirty

⸻

5. Drawing the Branches

\draw (S)--(W);
\draw (S)--(B);

These commands connect the starting point to the first-stage events.

Similarly,

\draw (W)--(WC);
\draw (W)--(WD);
\draw (B)--(BC);
\draw (B)--(BD);

connect each colour to its corresponding states.

⸻

6. Adding Probabilities

node[midway, above left] {$20/50$}

The node[midway,...] option places the probability label at the middle of a branch.

Different positioning options (above left and below left) are used to prevent labels from overlapping with the lines.

⸻

Output

The final diagram shows:

* A root (starting point)
* Two first-level outcomes: White and Black
* Two second-level outcomes for each colour: Clean and Dirty
* Probability values displayed on every branch

This is a basic example of a probability tree diagram created using TikZ.
