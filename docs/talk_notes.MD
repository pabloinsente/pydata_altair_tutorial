# Data Visualization with Altair: a grammar of graphics for Python

## Outline

- Two approaches to data visualization APIs: tell me how and tell me what
- Tell me how: imperative approach
- Tell me what: declarative approach
- Vega-Lite's unit specification: single Cartesian plot or single view
- Vega-Lite's multiple unit specification: multiple Cartesian plots or composite view
- Pros and a cons
- Examples

### Wilkinson's Grammar of graphics:
- Mathematical foundations for statistical graphics
- Postulate: taxonomies of charts are harmful
- A graphic is the representation of the graph of a function
- The rest is annotation around the graph
- Grammar: a system of rules to generate meaningful language statements
- In the context of graphics, grammar is a set of rules to generate perceivable graphics
- Taxonomies of charts, are like list of words: you can generate as many graphics as categories (words) in your taxonomy, but no more
- A grammar, is expressive and generative, allowing the creation of graphics beyond the limits of graph taxonomies
- Aesthetics "offers principles for relating sensory attributes (color, shape, sound, etc.) to abstractions"
- Charts are instances of more general objects: for instance, "a pie is a divided bar in polar coordinates, we can construct other polar graphics that are less well known"
- Computationally, implementing a grammar of graphics is better, because it allows reusability of general objects. Otherwise, each type of chart may requires new code and structures, making it unnecesarily complex

### Three main stages of graphic creation:

1. Specification
2. Assembly
3. Display

### Core elements of any statistical graphics specification:

- DATA: a set of data operations that create variables from datasets,
- TRANS: variable transformations (e.g., rank),
- SCALE: scale transformations (e.g., log),
- COORD: a coordinate system (e.g., polar),
- ELEMENT: graphs (e.g., points) and their aesthetic attributes (e.g., color)
- GUIDE: one or more guides (axes, legends, etc.)

"These components link data to objects and
specify a scene containing those objects"

## How Altair works:

- Crated by Jake VanderPlas and Brian Granger
- Altair is a declarative statistical visualization library for Python
- Based on Vega-Lite and Vega
- VEGA: Vega is a visualization grammar, a declarative language for creating, saving, and sharing interactive visualization designs
- VEGA-Lite: Vega-Lite is a high-level grammar of interactive graphics (High level API for Vega)

"Altair’s Python API emits Vega-Lite JSON data, which is then rendered in a user-interface such as the Jupyter Notebook, JupyterLab, or nteract using the Vega-Lite JavaScript library. Vega-Lite JSON is compiled to a full Vega specification (Satyanarayan, Russell, Hoffswell, & Heer, 2016), which is then parsed and executed using a reactive runtime that internally makes use of D3.js (Bostock, Ogievetsky, & Heer, 2011)"

## Vega primitives:
- Data
- Transforms
- Scales
- Guides
- Marks

## Vega-Lite:

### Description:
- Building blocks for composing an expressive range of graphics
- Design space based on an algebra of graphics is richer than design space based on taxonomies
- Facilitates rapid exploration and concise specification by ignoring low level details
- Paradox: conciseness generates more ambiguity. Vega-Lite resolves this by selecting sensible defaults
- Trade-off of control and customization vs conciseness and development speed
- Infer sensible defaults but with flexibility to change default values
- Vega-Lite draws from Wilkinson's grammar and Polaris/Tableu
- Allows for interactivity
- When you go on customizing the defaults, now the API start to look more imperative (how to do things)
- **Composition operators**: facet, layer, concatenate, repeat
- Do example of composed view (facet, repeat, layer, and repeated layer)
- Idea: hierarchical composition

### Vega-Lite's Unit Specification:
- single Cartesian plot with:
  - data set
  - mark-type
  - set of encodings for visual channels such as:
    - position (x,y)
    - color
    - size
    - etc

### Basic components:
- Data: input data to visualize, a relational table consisting of rows and columns.
- Transforms: data can be subject to trans such as filter, aggregation, binning, etc
- Mark: specifies the geometric object to visually encode data-records such as bar, line, area, text, rule, and symbols (point and tick)
- Encoding: mapping between data attributes (cols) and properties of visual marks such as position (x, y), color, shape, size, and text.
- Scale: functions that map data values to visual values
- Guides: Axes and legends that visualize scale. For x and y channels, either a linear scale (for quantitative data) or an ordinal scale (for ordinal/nominal data) is instantiated, along with an axis. For color, size, and shape channels, suitable palettes and legends are generated.

### Vega-Lite's Multiple Unit Specification:
Composition operators:
- Layer: produce a view in which charts are plotted on top of each other
- Concatenation: "glue" together any kind of views vertically or horizontally
- Facet: produces a trellis plot by sub-setting the data by the distinct values of a field. For quant variables scales and axes are shared by default.
- Repeat: "The repeat operator generates multiple plots, but unlike facet allows full replication of a data set in each cell." For instance, different representations of the same data

Nested views:
- composed views can be subsequently composed into more complex views
