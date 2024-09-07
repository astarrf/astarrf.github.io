---
math: true  # enable math mode
title: Tricks for better looking $\LaTeX$
#date: YYYY-MM-DD HH:MM:SS +0800
categories: [Note]
tags: [latex,note,en]     # TAG names should always be lowercase
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
> the '120' in `\put(-10,120){\textbf{b)}}` is not the same for all the figures. You should find the proper number.
{: .prompt-warning}

## Floating Figure/Table Surrounded by Text
If you want to have more freedom in showing the figure, you can try `\usepackage{subcaption,graphicx,wrapfig}`
Then, use this to insert figure:
```latex
\begin{wrapfigure}{l}{4.8cm} % 靠文字内容的左侧
\begin{minipage}[b]{.32\textwidth}
  \centering
  \includegraphics[width=.95\linewidth]{fig1.png}  
  \begin{picture}(0,0)
    \put(-140,95){\textbf{a)}}
  \end{picture}
  \phantomsubcaption
  \label{fig:fig1}
\end{minipage}
\begin{minipage}[b]{.32\textwidth}
  \centering
  \includegraphics[width=.95\linewidth]{fig2.png}  
  \begin{picture}(0,0)
    \put(-140,95){\textbf{b)}}
  \end{picture}
  \phantomsubcaption
  \label{fig:fig2}
\end{minipage}
\caption{Caption}
\label{fig:fig}
\end{wrapfigure}
```
This also include the subfigure and the 'a)', 'b)' text.
> There may be errors when referring the figures.
{: .prompt-warning}

For tables, things are similar to figure with `wraptable` instead of `wrapfigure`:
```latex
\begin{wraptable}{r}{6cm} 
\vspace{-6mm}
 \centering \caption{Table Caption}\label{tab:table}
 \vspace{-2mm}
\begin{tabular}{ccc}
    \hline
    a & b & c \\
    \hline
    $1$ & $2$ & $3$ \\
    $4$ & $5$ & $6$ \\
    \hline
   \end{tabular}
\vspace{-2mm}
\end{wraptable}
```
