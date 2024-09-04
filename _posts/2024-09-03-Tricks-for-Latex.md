---
math: true  # enable math mode
title: Tricks for better looking $\LaTeX$
#date: YYYY-MM-DD HH:MM:SS +0800
categories: [Note]
tags: [latex,note]     # TAG names should always be lowercase
---

## Better Subfigure
required package: `\usepackage{subcaption,graphicx}`
```
\begin{figure}[ht]
\centering
\begin{minipage}[b]{.45\textwidth}
  \centering
  \begin{picture}(0,0)
    \put(-10,120){\textbf{a)}}
  \end{picture}
  \includegraphics[width=.95\linewidth]{fig1.png}  
  \phantomsubcaption
  \label{fig:fig1}
\end{minipage}
\begin{minipage}[b]{.45\textwidth}
  \centering
  \begin{picture}(0,0)
    \put(-10,120){\textbf{b)}}
  \end{picture}
  \includegraphics[width=.95\linewidth]{fig2.png}  
  \phantomsubcaption
  \label{fig:fig2}
\end{minipage}
\caption{Caption}
\label{fig:fig}
\end{figure}
```
which looks like this:
![](/assets/img/Tricks-for-Latex/image.png)

**Caution**: the '120' in `\put(-10,120){\textbf{b)}}` is not the same for all the figures. You should find the proper number.
