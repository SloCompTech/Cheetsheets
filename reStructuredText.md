# reStructuredText
[Docs](http://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html)  
[Simple docs](https://thomas-cokelaer.info/tutorials/sphinx/rest_syntax.html)  
[Reference](http://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html?highlight=warning)

## Inline markup
```
*italic*
**bold**
``code samples``
```
**Note:** No spaces before and after, don't nest

## Titles
```
*****
Title
*****

Subtitle
********

===========
Subsubtitle
===========

```
**Note:** Same length as text

## Lists
```
* This is a bulleted list.
* It has two items, the second
  item uses two lines.

    * with a nested list
    * and some subitems

1. This is a numbered list.
2. It has two items too.
```
**Note:** Nested list must be separated with **blank** lines (top & bottom)

## Literal block
```
This is a normal text paragraph. The next paragraph is a code sample::

   It is not processed in any way, except
   that the indentation is removed.

   It can span multiple lines.

This is a normal text paragraph again.

.. literalinclude:: filename
    :linenos:
    :language: python
    :lines: 1, 3-5
    :start-after: 3
    :end-before: 5

    <code>
```

## Table
```
+------------------------+------------+----------+----------+
| Header row, column 1   | Header 2   | Header 3 | Header 4 |
| (header rows optional) |            |          |          |
+========================+============+==========+==========+
| body row 1, column 1   | column 2   | column 3 | column 4 |
+------------------------+------------+----------+----------+
| body row 2             | ...        | ...      |          |
+------------------------+------------+----------+----------+
```

## Code block
```
.. code-block:: ruby

   Some Ruby code.
```

## Hyperlinks
```
.. _label:      # Label

label_          # Link to label

:ref:`label`    # Link to label

`Unline link <https://domain.invalid/>`_

This is a paragraph that contains `a link`_.

.. _a link: https://domain.invalid/
```
**Note:** There must be space between text and `<`.

[See more](http://www.sphinx-doc.org/en/master/usage/restructuredtext/roles.html#ref-role)

## Boxes
```
.. seealso:: This is a simple **seealso** note.

.. note::  This is a **note** box.

.. warning:: note the space between the directive and the text

.. todo:: todo text

.. versionadded:: 2.5
   The *spam* parameter.

.. versionchanged:: 2.5
   The *spam* parameter.

.. deprecated:: 3.1
   Use :func:`spam` instead.


```

## Image
```
. image:: stars.jpg
    :width: 200px
    :align: center
    :height: 100px
    :alt: alternate text

.. figure:: stars.jpg
    :width: 200px
    :align: center
    :height: 100px
    :alt: alternate text
    :figclass: align-center

    figure are like images but with a caption

    and whatever else youwish to add

    .. code-block:: python

        import image
```

## Table of Contents
```
.. toctree::
    :maxdepth: 2
    :numbered:
    :titlesonly:
    :glob:
    :hidden:

    intro.rst
    chapter1.rst
    chapter2.rst
```

## CSV table
```
.. csv-table:: a title
   :header: "name", "firstname", "age"
   :widths: 20, 20, 10

   "Smith", "John", 40
   "Smith", "John, Junior", 20
```

## Footnotes
```
Lorem ipsum [#f1]_ dolor sit amet ... [#f2]_

.. rubric:: Footnotes

.. [#f1] Text of the first footnote.
.. [#f2] Text of the second footnote.
```

## Comments
Any invalid markup block
```
..
   This whole indented block
   is a comment.

   Still in the comment.
```

## Author
```
.. sectionauthor:: Guido van Rossum <guido@python.org>
.. codeauthor:: Guido van Rossum <guido@python.org>
```

## Index
```
.. index::
   single: execution; context
   module: __main__
   module: sys
   triple: module; search; path

The execution context
---------------------

...
```