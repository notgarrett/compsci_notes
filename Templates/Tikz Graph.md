```tikz
\definecolor{myRed}{RGB}{255,0,0} % Define your own red
\definecolor{myGreen}{RGB}{0,255,0} % Define your own red
\definecolor{myBlue}{RGB}{0,0,255} % Define your own red
\begin{document}
  \begin{tikzpicture}[domain=0:4]
    \draw[very thin,color=myBlue] (-0.1,-1.1) grid (3.9,3.9);
    \draw[->] (-0.2,0) -- (4.2,0) node[right] {$x$};
    \draw[->] (0,-1.2) -- (0,4.2) node[above] {$f(x)$};
    \draw[color=myBlue]    plot (\x,\x)             node[right] {$f(x) =x$};
    \draw[color=myGreen]   plot (\x,{sin(\x r)})    node[right] {$f(x) = \sin x$};
    \draw[color=myRed] plot (\x,{0.05*exp(\x)}) node[right] {$f(x) = \frac{1}{20} \mathrm e^x$};
  \end{tikzpicture}
\end{document}
```
