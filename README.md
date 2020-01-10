# Data Visualization with Altair: a grammar of graphics for Python

This a talk and interactive tutorial about Altair 4.0

Altair provides a elegant and consistent API for statistical graphics. Altair is built on top of the Vega-Lite high-level grammar for interactive graphics which is based on the "grammar of graphics" idea proposed by Leland Wilkinson. Altair's key strength is the provision of clear mental model based on a set of graphical primitives and carefully designed combinatoric rules, that yields an ample space of graphical displays, avoiding the constrains of chart taxonomies.

In this talk/tutorial, we will learn the fundamental building blocks of Altair/Vega-Lite's interface and design.

## Usage

### Option 1: Cloud-based environment (prefered)

Click in the ```binder``` icon -> [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/pabloinsente/pydata_altair_tutorial/078bfb1af4b01d5e4d1d89fef0904eecdfcc5778/?urlpath=lab).  

This will build a docker image of the repo that runs on the cloud. Beware that it may take 2-3 minutes to be ready.

Then navigate to the `notebooks` directory and click on `altair_tutorial_pydata_madison_2020.ipynb`

### Option 2: Local environment

To obtain the files locally, run this in the command line:

```
git clone https://github.com/pabloinsente/pydata_altair_tutorial.git
```

To set up your system, you need python 3.7 or higher installed in a Linux/Mac machine. The code should work on Windows machines with minor changes (but I haven't tested it). It is recommended to use a virtual environment before installing the dependencies. To do this, navigate into the cloned repository in the console by:

```bash
cd pydata_altair_tutorial
```

Note that you may need to change the path to cd into the directory.  

 Then run this inside that directory to create the virtual environment:

```Python
python3 -m venv venv
```

And activate your environment by running:

```bash
source venv/bin/activate
```

Install dependencies by running:

```Python
pip install -r requirements.txt
```


**To run the notebook**, navigate to the ```notebooks``` directory and launch Jupyter Lab as:

```Python
jupyter lab altair_tutorial_pydata_madison_2020.ipynb
```
