TikZ Venn Diagram Explanation

This LaTeX code uses the TikZ package to draw a three-set Venn diagram inside a universal set. It also highlights the intersection between the Badminton and Football sets.

Code Breakdown

1. Required Packages

\usepackage{tikz}
\usepackage{amsmath}

* tikz is used for drawing graphics and diagrams.
* amsmath provides mathematical symbols, including \xi.

⸻

2. Universal Set

\draw (-3.2, -2.8) rectangle (3.2, 2.6);
\node at (-3.4, 2.0) {$\xi$};

* Draws a rectangle representing the Universal Set.
* Places the symbol ξ outside the rectangle to denote the universal set.

⸻

3. Shading the Intersection

\begin{scope}
    \clip (-0.9, 0.5) circle (1.5);
    \fill[black] (0.9, 0.5) circle (1.5);
\end{scope}

This is the most important part of the code.

* \clip restricts the drawing area to the Badminton circle.
* \fill draws the Football circle in black.
* Since the drawing is clipped, only the overlapping region between the two circles becomes visible.

As a result, only the intersection of Badminton and Football is shaded.

⸻

4. Drawing the Three Sets

\draw (-0.9, 0.5) circle (1.5);
\draw (0.9, 0.5) circle (1.5);
\draw (0, -0.8) circle (1.5);

These commands draw three circles representing:

* Badminton (left)
* Football (right)
* Cricket (bottom)

Each circle has a radius of 1.5 units.

⸻

5. Adding Labels

\node at (-1.8, 2.2) {\textbf{badminton}};
\node at (1.8, 2.2) {\textbf{Football}};
\node at (0, -2.5) {\textbf{Cricket}};

These commands place bold labels near each circle for easy identification.

⸻

Output

The final diagram contains:

* A rectangle representing the Universal Set (ξ).
* Three overlapping circles for Badminton, Football, and Cricket.
* The intersection of Badminton and Football shaded in black.
* Clear labels for all three sets.

This technique demonstrates how \clip and \fill can be combined in TikZ to highlight specific regions of a Venn diagram.
