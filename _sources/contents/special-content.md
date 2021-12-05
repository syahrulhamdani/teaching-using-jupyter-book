# Special Contents in Jupyter Book

{cite:p}`jb` A common use of directives and roles is to create **special contents**.

```{note}
All of below contents are adapted from [Jupyter Book](https://jupyterbook.org/content/index.html) documentation {cite:p}`jb`.
```


## Notes, Warnings, and Other Adminitions

* Notes

````
```{note}
This will be a note
```
````

will render:

```{note}
This will be a note
```

* Warnings

````
```{warning}
There's a warning!
```
````

will render:

```{warning}
There's a warning!
```

* Error

````
```{error}
Found some errors
```
````

will render:

```{error}
Found some errors
```

* Custom Admonition

````
```{admonition} This is an admonition
here's the content inside an admonition
```
````

```{seealso}
For a complete list, see the [sphinx-book-theme documentation](https://sphinx-book-theme.readthedocs.io/en/latest/reference/kitchen-sink/paragraph-markup.html#admonitions).
```


## Panels

Panels help us to organize chunks of content into flexible containers on page in a card-like layout.	

```{panels}
**Supervised**
^^^
Type of machine learning where the data have a target variable or the ground truth.
---
**Unsupervised**
^^^
Type of machine learning where the data doesn't have a target variable.
```


## Quotations

If you've used Jupyter Notebook/Lab, you may have used a quotation with syntax `>`. Jupyter Book also has the same quotation.

`````{panels}
Source
^^^
````
```
> A quotation just like notebook and lab.
```
````
---
Result
^^^
> A quotation just like notebook and lab.
`````

The result will look like this:

> A quotation just like notebook and lab
>
> from Jupyter Book

Moreover, Jupyter Book also provide a medium-like quotation using a directive `{epigraphh}`.

`````{panels}
Source
^^^
````
```{epigraph}
A medium-like quotation which is awesome!
```
````
---
Result
^^^
```{epigraph}
A quotation just like notebook and lab.
```
`````

The result will look like this:

```{epigraph}
A quotation just like notebook and lab.

from Jupyter Book
```

or you can have something like this:

```{epigraph}
A quotation just like notebook and lab.

-- Jupyter Book
```

The above `epigraph` is generated using below syntax.

````
```{epigraph}
A quotation just like notebook and lab.

-- Jupyter Book
```
````


## Tabbed Content

This is, for me, is the best feature in Jupyter Book. We can create a tabbed content when we want to, for example, compare codes using different library/language.
This can be done using directive `{tabbed}`.

Below syntax,

`````
````{tabbed} OpenCV
```python
import cv2

image = cv2.imread("path/to/image")
```
````

````{tabbed} Pillow
```python
from PIL import Image

image = Image.open("path/to/image")
```
````
`````

will result in

````{tabbed} OpenCV
```python
import cv2

image = cv2.imread("path/to/image")
```
````

````{tabbed} Pillow
```
from PIL import Image

image = Image.open("path/to/image")
```
````


## Images and Figures

We can still use the usual syntax to include image like `![](../assets/images/pycon-bright-1.png)`, which will render to

![](../assets/images/pycon-bright-1.png)

Another syntax we can use to include images is to use `{image}` directive. With this, we can have more flexibility in configuring the width, alignment, etc.

```{image} ../assets/images/pycon-bright-1.png
:alt: PyCon Logo
:width: 50%
:align: center
```

The above image is rendered from this syntax.

````
```{image}
:alt: PyCon Logo
:width: 50%
:align: center
```
````


Now, Jupyter Book through MyST Markdown include `{figures}` directive. Figures are just like images, except they are easier to reference and include an image caption with numbering.

Below figure,

```{figure}  ../assets/images/pycon-bright-1.png
:alt: PyCon Logo
:name: pycon-bright-fig
:width: 50%
:align: center

A PyCon Indonesia 2021 logo.
```

is generated using below syntax

````
```{figure}  ../assets/images/pycon-bright-1.png
:alt: PyCon Logo
:name: pycon-bright-fig
:width: 50%
:align: center

A PyCon Indonesia 2021 logo.
```
````

The `name` key in the directive `{figure}` is used for reference. So, we can use `` {ref}`pycon-bright-fig` `` to go back to the image: {ref}`pycon-bright-fig`.
