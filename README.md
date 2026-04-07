# GeoenergiaTexAndTikz

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Overview

This repository contains the **TikZ source code** for plots, figures, and diagrams frequently used by members of the **Geoenergia Lab** (Department of Petroleum Engineering, Santa Catarina State University, Brazil).  

**You are meant to use the TikZ source files directly** – copy the code into your own LaTeX documents, modify colours, resize, adapt to your needs. The pre‑compiled PDFs shown below are only for **preview**; they are **not** the primary deliverable.

## Preview of included figures

Here is an example generated from `Tikz/CollisionStreamingDiagram.tex` (LBM collision and streaming, D2Q9):

![LBM collision and streaming (preview)](Figs/CollisionStreamingDiagram.pdf)

> ⚠️ The image above is just a preview. **To use this figure in your own work**, copy the source code from `Tikz/CollisionStreamingDiagram.tex` into your document or use `\input{Tikz/CollisionStreamingDiagram.tex}` (after loading required packages).

## How to use the TikZ code

### Option A – Copy the code directly

Open any `.tex` file from the `Tikz/` folder, copy the `tikzpicture` environment (and any required `\usetikzlibrary` commands), and paste it into your LaTeX document.

### Option B – Input the file (requires `standalone` package)

If you keep the repository as a subfolder, you can input the figure source directly:

```latex
\documentclass{article}
\usepackage{tikz}
\usetikzlibrary{arrows.meta}   % (add libraries as needed)
\usepackage{standalone}         % allows input of standalone files

\begin{document}
\begin{figure}
  \centering
  \input{Tikz/CollisionStreamingDiagram.tex}
  \caption{LBM collision and streaming steps.}
\end{figure}
\end{document}
