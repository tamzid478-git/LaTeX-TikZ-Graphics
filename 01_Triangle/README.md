# 📐 Geometry Visualization with TikZ

A geometric triangle construction demonstration using the **tkz-euclide** package in LaTeX.

### 💡 LaTeX Code:

```latex
\documentclass{article}
\usepackage{tikz}
\usepackage{tkz-euclide}   

\begin{document}
\begin{tikzpicture}
\draw [lightgray] (0,0) grid (10,10);     
\coordinate [label=left:$p$] (p) at (3,1);   
\coordinate [label=right:$r$] (r) at (8,1);
\coordinate [label=above:$q$] (q) at (5.5,6);
\draw [very thick,red] (p) -- (q) -- (r) -- cycle;
\tkzLabelSegment [below](p,r) {$8cm$};
\tkzLabelSegment [above right=2pt](q,r) {$x$ cm};
\tkzMarkAngle [size=1.4cm](r,p,q);
\tkzLabelAngle (r,p,q) {$60^{\circ}$};
\tkzMarkAngle[size=2cm](p,q,r);
\tkzLabelAngle[pos=1.25](p,q,r){$40^{\circ}$};
\tkzMarkAngle [size=2cm](q,r,p);
\tkzLabelAngle (q,r,p) {$80^{\circ}$};
\end{tikzpicture}
\end{document}
