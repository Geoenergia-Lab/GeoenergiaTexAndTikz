# Geoenergia Tex and TikZ

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)

## Overview

This repository contains the **TikZ source code** for plots, figures, and diagrams frequently used by members of the **Geoenergia Lab** (Department of Petroleum Engineering, Santa Catarina State University, Brazil).  

**You are meant to use the TikZ source files directly** – copy the code into your own LaTeX documents, modify colours, resize, adapt to your needs. The pre‑compiled PDFs shown below are only for **preview**; they are **not** the primary deliverable.

## Preview of included figures

Here is an example generated from `Tikz/CollisionStreamingSteps.tex` (LBM collision and streaming, D2Q9):

![LBM collision and streaming (preview)](Figs/CollisionStreamingSteps.png)

> ⚠️ The image above is just a preview. **To use this figure in your own work**, copy the source code from `Tikz/CollisionStreamingSteps.tex` into your document or use `\input{Tikz/CollisionStreamingSteps.tex}` (after loading required packages).

## Getting started on Overleaf

You can **import this repository directly into Overleaf** and use it as a starting point for your own projects:

1. In Overleaf, click **New Project** → **Import from GitHub**.
2. Authorise Overleaf and select this repository (`GeoenergiaTexAndTikz`).
3. Overleaf will clone the repo, and you can immediately edit the TikZ figures or the showcase document.

## Contributing new figures

If you create a new TikZ figure that you think should be part of the lab’s collection, you can **contribute back** using Overleaf’s GitHub integration:

1. **Import the repository into Overleaf** (as described above).
2. Add your new `.tex` file(s) to the `Tikz/` folder (or update existing ones).
3. Compile and test that everything works.
4. Open the left‑hand panel in Overleaf → **Integrations** → **GitHub**.
5. Write a commit message describing your changes and click **Push changes**.

Your new figure will appear in the GitHub repository after the push.  
(If you are not familiar with Git, Overleaf’s GitHub integration handles everything for you.)

Alternatively, you can clone the repository locally, add your files, and push via normal Git commands.

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
