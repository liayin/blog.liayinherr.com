---
layout: post
title: LaTeX Figures
date: 2023-5-23 1:22:01 --0000
permalink: /posts/latex-figures/
---
(Updated 12/2/2025)

This blog post covers the basics of LaTeX figures. 

```LaTeX
\begin{figure}[H]
    \vspace{4mm}
    \centering
    \caption{Effect of Law on Murder Over Time}
    \label{fig:event_study_murder}
    \includegraphics[scale=.5]{figures_tables/event_study_murderrate.png}
    \vspace{-4mm}
    \caption*{\footnotesize \textit{Notes}: This figure reports the results from event study analysis of the SYG laws on murder. It plots both the point estimates and their 95 percent confidence intervals. Standard errors are clustered by the state. The years after the laws pass witness an increase in murder, and the effects are larger and persistent.}
    \vspace{4mm}
\end{figure}
```