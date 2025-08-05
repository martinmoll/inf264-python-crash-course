# INF264 – Python Crash Course – An Introduction to NumPy and Matplotlib <!-- omit from toc --> 

Welcome to the INF264 Python crash course. This repository contain guides (Jupyter notebooks) to help you get familiar with NumPy and Matplotlib, two Python libraries required for completing homeworks and the two mandatory projects in INF264.

If you encounter any problems, feel free to ask a group leader or post your questions in the Discord channel `#python-crash-course` on our Discord server.

## Prerequisites <!-- omit from toc --> 

We will assume that you are familiar with the basics of Python programming including topics such as data types and structures, conditional statements, functions, loops etc. If you feel you need to brush up on your Python skills, have a look at the free online course [Python Programming MOOC 2023](https://programming-23.mooc.fi/) (part 1 – 7).

## Table of Contents <!-- omit from toc --> 
- [Installing Required Software for INF264](#installing-required-software-for-inf264)
  - [1. Installing Anaconda](#1-installing-anaconda)
  - [2. Create an Environment](#2-create-an-environment)
  - [3. Managing the Environment](#3-managing-the-environment)
- [Course Content](#course-content)
  - [What is NumPy?](#what-is-numpy)
  - [What is Matplotlib?](#what-is-matplotlib)
  - [Notebooks with Examples and Exercises](#notebooks-with-examples-and-exercises)

# Installing Required Software for INF264

## 1. Installing Anaconda

To install Anaconda, click the link below corresponding to your operating system and follow the instructions there.

- [Windows](https://docs.anaconda.com/free/anaconda/install/windows/)
- [macOS](https://docs.anaconda.com/free/anaconda/install/mac-os/)
- [Linux](https://docs.anaconda.com/free/anaconda/install/linux/)

## 2. Create an Environment

We will now create a new Anaconda environment for INF264.

1. Open a terminal window.
2. Run the command `conda create --name=INF264 python` to create a new environment named `INF264` with the latest Python version.
3. Run the command `conda activate INF264` to activate the newly create environment.
4. Run `conda install -c conda-forge numpy scikit-learn jupyter pandas matplotlib ipykernel` to download and install the required packages. 

To test that everything is working as expected, create a new notebook by running `jupyter-lab` (if you use VS Code, see below) and create and run a code cell with the following content:

```python
import sklearn
import numpy
import pandas
import matplotlib.pyplot
```

**Notebooks in VS Code Instructions**

If your are using VSCode, you can also work with Jupyter notebooks there.


1. Install the *Jupyter* extension in VS Code (if you do not have it).
2. Create a new file `File >> New File ...` and choose `Jupyter Notebook`.
3. Click `Select Kernel` in the upper right corner and choose the kernel `INF264` that we created using Anaconda.
4. Edit the code cell by clicking on it and paste the above code with imports.
5. Press the "play button" on the cell (or `Ctrl + Enter`) to run the code cell.
6. If everything is installed properly, you should see no error messages.

![animation showing how to create a jupyter notebook in vs code](figs/create_notebook_vs_code.gif)


**Useful notebook shortcuts:**
- Arrow keys to navigate between cells.
- `Shift + Enter` to run the current cell and move to the next one.
- `Ctrl + Enter` to run the current cell and stay in the same cell.
- `Esc` to enter command mode.
- `Enter` to enter edit mode.
- `A` to insert a new cell above the current cell.
- `B` to insert a new cell below the current cell.
- `DD` to delete the current cell.
- `M` to change the current cell to a Markdown cell.
- `Y` to change the current cell to a code cell.



## 3. Managing the Environment

Enter the environment by running `conda activate INF264`. To exit the `INF264` environment, simply run `conda deactivate`.

(Optional) To update all packages in your environment, run `conda update --all` (when the environment is already activated).

(Optional) At the end of the semester, if you want to clean up and delete the `INF264` environment from your system, run the command `conda env remove --name INF264`.

# Course Content

The course content mainly consists of Jupyter notebooks (see below) containing many examples and some exercies to help you get familiar with both NumPy and Matplotlib.

## What is NumPy?

**NumPy**, short for Numerical Python, is a powerful library for numerical computing in Python. It provides support for arrays, matrices, and many mathematical functions to operate on these data structures efficiently.

For more details about the differences and advantages of using NumPy arrays as oposed to Python lists when working with numerical data, see ["What is NumPy?"](https://numpy.org/doc/stable/user/whatisnumpy.html) from the NumPy documentation.

It is convention to import NumPy under the alias `np` by writing

```python
import numpy as np
```

in the beginning of the Python file or notebook where you want to use NumPy functions.

The (very useful) NumPy documentation can be found [here (link)](https://numpy.org/devdocs/).

## What is Matplotlib?

**Matplotlib** is a popular and flexible library for creating many types of data visualizations and plots.

It is convention to import matplotlib's pyplot module under the alias `plt` by writing

```python
import matplotlib.pyplot as plt
```

The documentation for matplotlib can be found [here (link)](https://matplotlib.org/stable/index.html).


## Notebooks with Examples and Exercises

You can download all the notebooks by downloading this repository as a ZIP file (see screenshot below), or use `git clone` if you are familiar with git.

![Download zipped repo](figs/download_repo.png)

If you use VS Code, go to `File >> Open Folder...` and choose the directory `notebooks` (after unzipping the repository). Remember to choose the `INF264` environment as the kernel for the notebooks.

**NumPy Notebooks**

1. [Creating NumPy Arrays](notebooks/numpy_001.ipynb)
2. [Indexing NumPy Arrays](notebooks/numpy_002.ipynb)
3. [Reshaping, Transposing and Concatenating Arrays](notebooks/numpy_003.ipynb)
4. [Basic Array Operations and Broadcasting](notebooks/numpy_004.ipynb)
5. [Matrix and Vector Algebra in NumPy](notebooks/numpy_005.ipynb)
6. [Reduction Operations in NumPy](notebooks/numpy_006.ipynb)
7. [Other Useful NumPy Functions](notebooks/numpy_007.ipynb)

It is recommended to work through the NumPy notebooks in the order they are listed.

**Matplotlib Notebook**

Download and go through the notebook [A Short Introduction to Matplotlib](notebooks/matplotlib_001.ipynb).

**Solutions**

You are encouraged to try to complete all the exercises on your own. If you get completly stuck, notebooks with solutions can be found in the directory `notebooks/with_solutions`.
