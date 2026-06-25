---
layout: post
title: notebooks for R and Octave 
date: 2021-11-25
description: how to setup and use notebooks for R and Octave
---

[Jupyter](https://jupyter.org/) notebooks were created for Julia and Python languages. However, they are not restricted to these two languages and by loading the appropriate kernels---there are currently over 100 available---one can execute C, C++, C#, Fortran, Java, R, Julia, Matlab, Octave, Scheme, Processing, Scala, and many more.

Why use Jupyter notebooks?

1. Everyone is using them.
2. They enable shareable, reproducible research.
3. They write the report for you... OK, they faciltate the fusion of text, code and results in a single, publication quality reprot. In particular, they accept LaTeX-type commands for nice math typesetting.

Here, I will show how to install and use the R, Julia and Octave kernels, since Python is already installed by default.


The basic install uses either `pip` or `conda` as follows:

````
conda install -c conda-forge notebook
````

or

````
pip install notebook
````

I personally prefer the newer interface, 

````
pip install jupyterlab
````

Once installed, launch a notebook, that will appear in your default browser, by

````
jupyter notebook
````

or

````
jupyter-lab
````

### R kernel installation and use

1. Install [R](https://www.r-project.org/).
2. Run R, and execute the commands
	````
	install.packages('IRkernel')
	IRkernel::installspec(user = FALSE)
	````
3. In a system command window, launch a notebook and choose the `R` kernel from the `New` dropdown menu.

### Octave kernel installation and use

1. Install the kernel directly into Jupyter with the command
   ````
   pip install octave_kernel
   ````
2. Add the Octave executable to your system path - this is OS-dependent...
3. Launch a notebook and choose the `octave` kernel from the `New` dropdown menu.

An example can be found [here](https://nbviewer.org/github/Calysto/octave_kernel/blob/master/octave_kernel.ipynb). Various troubleshooting issues can be found [here](https://github.com/calysto/octave_kernel).

### Julia kernel installation and use

1. Install [Julia](https://julialang.org/downloads/)
2. Run Julia, and execute the following at the command-line:
  - `using Pkg`
  - `Pkg.add("IJulia")`
3. Launch a notebook and choose the `julia` kernel from the `New` dropdown menu.
 

