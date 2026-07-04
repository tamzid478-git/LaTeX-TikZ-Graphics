# 📐 Geometry Visualization with TikZ

A geometric triangle construction demonstration using the **tkz-euclide** package in LaTeX.

### 📋 Overview
This project visualizes a triangle with specific dimensions and internal angles. It utilizes a grid system for precise coordinate placement and geometric labeling.

---

### 💡 Code Explanation

The following key components were used to build this visualization:

* **`\usepackage{tkz-euclide}`**: This package is essential for handling Euclidean geometry in LaTeX, allowing for precise point and angle definitions.
* **`\draw [lightgray] (0,0) grid (10,10);`**: Creates a background grid to ensure accuracy while positioning the triangle vertices.
* **`\coordinate [label=...]`**: Defines the three vertices of the triangle ($p, q, r$) at specific coordinate points and assigns them labels.
* **`\draw [very thick,red] (p) -- (q) -- (r) -- cycle;`**: Connects the points to form the triangle. The `cycle` command ensures the path closes back to the first point.
* **`\tkzLabelSegment`**: Used to annotate the side lengths of the triangle ($8cm$ and $x\ cm$).
* **`\tkzMarkAngle` & `\tkzLabelAngle`**: These commands calculate and draw the arcs for the internal angles ($60^{\circ}, 40^{\circ}, 80^{\circ}$) and place the labels at the correct positions.

---

### 🖼 Visualization Output
*(Please refer to the PDF or image file included in this folder for the rendered output.)*

---
*Created as part of my LaTeX/TikZ learning journey.*
