%title: PyData - Madison
%author: Pablo Caceres - 01-23-2020
%date: 01-23-2020


-> # Data Visualization with Altair: a grammar of graphics for Python <-

-> *Pablo Caceres* <-
-> *01-23-2020* <-
-> *pcaceres@wisc.edu* <-


-> ## Outline <-

<br>
1. Two approaches to data visualization APIs: tell me how and tell me what

<br>
2. Wilkinson's grammar of graphics

<br>
3. Altair, Vega-Lite, and Vega

<br>
4. Altair in Practice

***

-> # Two approaches to data visualization APIs: tell me how and tell me what <-


<br>
- **Imperative approach**: specifies the *_how_* (e.g., matplotlib):

<br>
    - _Pros_: **fine-graned control** over chart specification

<br>
    - _Cons_: **Verbose**, makes you think about low-level visualization details

<br>
- **Declarative approach**: specifies the *_what_* (e.g., altair, plotnine (ggplot2)):

<br>
    - _Pros_: fast development, conciseness, and lets you **concentrate on visualization content**

<br>
    - _Cons_: **less control** over chart details, trust someone elses decisions about low level graph properties

***

-> # Wilkinson's Grammar of graphics <-


<br>
- **Mathematical foundations** for statistical graphics

<br>
- Proposed a **grammar** to formalize his idea

<br>
- **Grammar of graphics**: a system of rules and primitives to generate meaninful perceivable graphics

<br>
- Postulate: **taxonomies of charts are harmful**

***

-> # Why a grammar instead of a taxonomy? <-


<br>
- **Taxonomies of charts are like list of words**: you can generate as many graphics as categories (words) in your taxonomy, but no more. Hence, is limiting.

<br>
- **A grammar is expressive and generative**: allows the creation of graphics beyond the limits of graph taxonomies

<br>
- Grammars **are not limitless** in their generativity, but the **space of graphical objects to be generated is larger**

***

-> # Core elements of any statistical graphics specification (Wilkinson) <-


<br>
- **DATA**: a set of data operations that create variables from datasets

<br>
- **TRANS**: variable transformations (e.g., rank)

<br>
- **SCALE**: scale transformations (e.g., log)

<br>
- **COORD**: a coordinate system (e.g., polar)

<br>
- **ELEMENT**: graphs (e.g., points) and their aesthetic attributes (e.g., color)

<br>
- **GUIDE**: one or more guides (axes, legends, etc.)

<br>
_Wilkinson_: *"These components link data to objects and specify a scene containing those objects"*

***

-> # Altair, Vega-Lite, and Vega <-


<br>
- **Altair**: a declarative statistical visualization library for Python, based on Vega-Lite and Vega. Created by **Jake VanderPlas** and **Brian Granger**

<br>
- **Vega-Lite**: Vega-Lite is a high-level grammar of interactive graphics (High level API for Vega)

<br>
- **Vega**: is a visualization grammar, a declarative language for creating, saving, and sharing interactive visualization designs

***

-> # How Altair works <-


<br>
- **Step 1**: Altair’s Python API emits Vega-Lite JSON data specification 

<br>
- **Step 2**: Vega-Lite JSON is compiled to a full Vega specification

<br>
- **Step 3**: Vega specification is then parsed and executed using a reactive runtime that internally makes use of D3.js

<br>
- **Step 4**: chart is rendered in a [user-interface](https://altair-viz.github.io/user_guide/display_frontends.html#display-general) such as the Jupyter Lab, VSCODE, and others

***

-> # Altair's/Vega-Lite's building blocks <-

<br>
- **Data**: input data to visualize, a relational table consisting of rows and columns.

<br>
- **Transforms**: data can be subject to transformations such as filter, aggregation, binning, etc

<br>
- **Marks**:  geometric object to visually encode data-records such as bar, line, area, text, rule, and symbols (point and tick)

<br>
- **Encodings**: mapping between data attributes (cols) and properties of visual marks such as position (x, y), color, shape, size, and text.

<br>
- **Scales**: functions that map data values to visual values

<br>
- **Guides**: Axes and legends that visualize scales (ordinal, quantitative, nominal)

***

-> # Important note <-

<br>
This tutorial/talk is based on a series of **online resources** that you may want to give a closer look: 

<br>
- [Wilkinson, L. (2005). The Grammar of Graphics. Springer](https://www.springer.com/gp/book/9780387245447)

<br>
- [VanderPlas, et all (2018). Altair: Interactive statistical visualizations for python. Journal of open source software, 3(32), 1057.](https://idl.cs.washington.edu/files/2018-Altair-JOSS.pdf)

<br>
- [Satyanarayan, A., Moritz, D., Wongsuphasawat, K., & Heer, J. (2016). Vega-lite: A grammar of interactive graphics. IEEE transactions on visualization and computer graphics, 23(1), 341-350.](https://idl.cs.washington.edu/files/2017-VegaLite-InfoVis.pdf)


***

**Talks/turorials:**

<br>
- [Dominik Moritz and Kanit Wongsuphasawat - Vega-Lite: A Grammar of Interactive Graphics](https://www.youtube.com/watch?v=Nsrz4YdaZ_A)

<br>
- [Jake VanderPlas - Exploratory Data Visualization with Vega, Vega-Lite, and Altair](https://www.youtube.com/watch?v=ms29ZPUKxbU)

<br>
- [Leland Wilkinson, H2O.ai - The Grammar of Graphics and the Future of Big Data Visualization](https://www.youtube.com/watch?v=1X93Sum_SyM)
