---
layout: post
title: 06 Introduction to NumPy 
---

We saw in the
[Introduction to Python]({{site.baseurl}}{%post_url 2020-01-30-04_Introduction_to_Python_2%})
that the Python language has the control and data structures to do
numerical calculations. For instance, a vector $$\mathbf{r} = \left(
\begin{array}{c}x\\ y\\ z \end{array} \right)$$
denoting the position of a particle could be represented as a Python
list `r = [x, y, z]` and a matrix $$\sigma_{y} = \left( \begin{array}{ccc} 0
& -i \\ i & 0 \end{array} \right)$$ as a list of lists `sigma_y =
[[0, -1j], [1j, 0]]`.

When it comes to doing numerical work, Python by itself is rather
slow. By slow we mean compared to languages like C and Fortran, which
benefit from being compiled languages in which a program is
preprocessed into machine code by a compiler. Python by contrast is an
interpreted language, in which each line in a program is fed to the
Python interpreter in sequence, then executed. The flexiblity and ease
of use that come with Python come at the cost of pure performance.

However, though Python code itself may be slow, Python can be used to
run code that is written in a compiled language and already
compiled. We will use a library (a.k.a., a [Python
**package**]({{site.baseurl}}{%post_url 2020-02-06-04_Introduction_to_Python_4%}#modules)) that does exactly
this underneath the hood to get fast performance for numerical
operations on arrays: We load the [NumPy](https://www.numpy.org/)
package:

{% highlight python %}
import numpy
{% endhighlight %}

We will learn the basics of [NumPy](https://www.numpy.org/) and
plotting with [matplotlib](https://matplotlib.org/).

## Class material

The class will be live-coded in a Jupyter notebook. The annotated
notebook is available as
[06-intro-numpy.ipynb]({{site.nbviewer.resources}}/06_numpy/06-intro-numpy.ipynb)
and [06-intro-matplotlib.ipynb]({{site.nbviewer.resources}}/06_numpy/06-intro-matplotlib.ipynb)

You can load the notebook yourself: first update your local
[PHY494-resources repository]({{site.resources.url}})[^0]

{% highlight bash %}
cd ~/PHY494-resources
git pull
{% endhighlight %}

Copy the notebooks to your work directory

{% highlight bash %}
cd
mkdir ~/PHY494/06_numpy
cd ~/PHY494/06_numpy
cp ~/PHY494-resources/06_numpy/06-intro-*.ipynb .
{% endhighlight %}


and launch the Jupyter notebook interface in your web browser[^1]:

{% highlight bash %}
jupyter notebook
{% endhighlight %}

Select the notebooks *06-intro-numpy.ipynb* and
*06-intro-matplotlib.ipynb* from the list. They run in separate
browser tabs.

### Jupyter notebook
Basic Jupyter notebook commands:

* Look at the **Help** menu! (see also the
  [Jupyter Notebook Online Help](http://nbviewer.jupyter.org/github/ipython/ipython/blob/3.x/examples/Notebook/Index.ipynb))
* A notebook has
  [two modes](http://nbviewer.jupyter.org/github/ipython/ipython/blob/3.x/examples/Notebook/Notebook%20Basics.ipynb#Modal-editor)
  * **edit mode**:
    * green box around a cell: you can type into the cell
    * enter edit mode by pressing `Enter` (or `Return`) or click on a
      cell
  * **command mode**:
    * gray box around a cell (you *cannot* type into a cell!)
    * keys perform many different actions (don't type randomly...),
      e.g., cursor keys move up/down, `c` copies a cell, `shift +
      enter` evaluates a cell.
	* enter command mode by pressing `ESC` or clicking outside a
      cell's area
* Evaluate a cell: in command mode (gray cells with blue side bar):  `shift + return`
* Change a cell type: menu (*code* is Python, *Markdown* is text in
  [Markdown](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/)
  format)


## Resources
* NumPy [Quickstart Tutorial](https://docs.scipy.org/doc/numpy/user/quickstart.html)
* Software Carpentry
  [Analysing data with numpy and matplotlib](http://swcarpentry.github.io/python-novice-inflammation-2.7/01-numpy.html)
* Software Carpentry
  [Advanced
  NumPy](http://paris-swc.github.io/advanced-numpy-lesson/index.html)
* **SciPy Lectures [1.3. NumPy: creating and manipulating numerical
  data](https://scipy-lectures.org/intro/numpy/)** by Emmanuelle
  Gouillart, Didrik Pinte, Gaël Varoquaux, and Pauli Virtanen. 
  
  (The [SciPy lectures](https://scipy-lectures.org) are an
  *outstanding learning resource* and if you only had one place on the
  internet to learn scientific programming in Python then this would
  be it!)


----------

#### Footnotes

[^0]:

    If you have not set up your PHY494-resources repository then
    revisit [Git Basics: Class resources]({{site.baseurl}}{% post_url
    2020-01-23-03_Git_basics %}#class-resources-on-github).

[^1]:

    If you have problems launching the notebook interface on Mac OS X,
    try

         jupyter notebook --ip=127.0.0.1

    If problems persist, google for the error message and ask for help.
