Exponential Growth Graph using TikZ

This LaTeX code uses the TikZ package to draw an Exponential Growth Graph representing the function

[
y = 2^x
]

The graph demonstrates how a quantity increases exponentially as time progresses.

Code Breakdown

1. Required Package

\usepackage{tikz}

Only the tikz package is required to draw the graph.

⸻

2. Scaling the Axes

\begin{tikzpicture}[x=1.5cm,y=0.35cm]

The x and y options scale the coordinate system.

* x=1.5cm stretches the horizontal axis.
* y=0.35cm compresses the vertical axis so that larger values fit comfortably on the page.

⸻

3. Drawing the Grid

\foreach \x in {1,...,4}

This loop creates the vertical grid lines and places tick marks on the x-axis.

Similarly,

\foreach \y in {1,2,4,8,16}

creates the horizontal grid lines and labels the y-axis.

Using \foreach avoids writing repetitive drawing commands.

⸻

4. Drawing the Axes

\draw[->,thick] (-0.5,0)--(5.5,0);
\draw[->,thick] (0,-0.5)--(0,18);

These commands draw the horizontal and vertical axes with arrowheads.

The axes are labeled as:

* time (t) on the x-axis
* size (y) on the y-axis

The origin is labeled with O.

⸻

5. Plotting the Function

\draw[red,ultra thick,domain=0:4.1,samples=100]
plot (\x,{2^\x});

This command plots the exponential function

[
y = 2^x.
]

* domain=0:4.1 specifies the interval over which the function is drawn.
* samples=100 generates 100 points, producing a smooth curve.
* red colors the graph red.
* ultra thick makes the curve more prominent.

⸻

Output

The final figure contains:

* A coordinate system with labeled axes.
* Light gray grid lines for easier reading.
* Tick marks on both axes.
* A smooth red curve representing the exponential function (y = 2^x).
* Labels for the origin and both axes.

This example demonstrates how TikZ can be used to create clean mathematical graphs directly in LaTeX without requiring external graphing software.
