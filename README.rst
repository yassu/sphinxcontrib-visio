===================
sphinxcontrib-visio
===================

`sphinxcontrib-visio` is a sphinx extension. It embeds MS-Visio file (.vsd, .vsdx) to your documents.

.. image:: https://travis-ci.org/visio2img/sphinxcontrib-visio.svg?branch=master
   :target: https://travis-ci.org/visio2img/sphinxcontrib-visio
   :alt: Build Status

.. image:: https://pypip.in/v/sphinxcontrib-visio/badge.png
   :target: https://pypi.python.org/pypi/sphinxcontrib-visio/
   :alt: Latest PyPI version

.. image:: https://pypip.in/d/sphinxcontrib-visio/badge.png
   :target: https://pypi.python.org/pypi/sphinxcontrib-visio/
   :alt: Number of PyPI downloads

Requirements
=============

* Python 2.7, 3.3 or later
* pywin32_
* visio2img_ 1.2.0 or later
* Microsoft Visio

.. _pywin32: http://sourceforge.net/projects/pywin32/files/pywin32/
.. _visio2img: https://pypi.python.org/pypi/visio2img

Setup
======

Install `sphinxcontrib-visio` package.

::

   $ pip install sphinxcontrib-visio

And then, append `sphinxcontrib.visio` to `conf.py` of your Sphinx project.

::

   # extensions = []
   extensions = ['sphinxcontrib.visio']

Directives
===========

**.. visio-image: [filename]**

   This directive inserts MS-Visio image into the document.
   It inserts image from visio file named as `filename`.

   Examples::

     .. visio-image:: foo.vsdx

   The `visio-image` directive supports all of the options of the `image` directive.

   In addition, the following options are recognized:

   ``page`` : number
      Page number of the page to embed to document.

   ``name`` : text
      Title of the page to embed to document.

**.. visio-figure: [filename]**

   This directive inserts MS-Visio image into the document and its caption.
   It inserts image from visio file named as `filename`.

   Examples::

     .. visio-figure:: foo.vsdx

        caption of foo

   The `visio-figure` directive supports all of the options of the `figure` directive.

   In addition, the following options are recognized:

   ``page`` : number
      Page number of the page to embed to document.

   ``name`` : text
      Title of the page to embed to document.

Author
=======

Yassu <yassumath@gmail.com>

Maintainer
===========

Takeshi KOMIYA <i.tkomiya@gmail.com>

License
========
Apache License 2.0