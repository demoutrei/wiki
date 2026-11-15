.. demoutrei's wiki documentation master file, created by
   sphinx-quickstart on Sun Nov 15 23:39:01 2026.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


Table of Contents
=================

.. toctree::
    :maxdepth: 1
    :caption: Artificial Intelligence

    Introductory <./artificial_intelligence/index.rst>


Contribution
++++++++++++

**demoutrei's wiki** is open for contributions.


Build Configuration
^^^^^^^^^^^^^^^^^^^

rST files must be added in the ``toctree`` directive of the relative ``index.rst`` in its directory. Each directory must contain an ``index.rst`` file, containing at most one ``toctree`` directive.

To execute the build, run the following command in a terminal:

.. code-block:: bash

    $ ./make.bat html


How Can I Contribute?
^^^^^^^^^^^^^^^^^^^^^


Pull Requests
~~~~~~~~~~~~~

Fork the repository, and create a branch of ``contrib/<username>``. Append your contribution and secure that it follows our style standards. Before you issue a Pull Request (PR), make sure it builds with no exceptions or warnings.


Others
~~~~~~

You are recommended to open a Discussion for topics you want to talk about, or something to clarify with; or an Issue regarding something that's already deployed in the wiki.


Guide Standards
^^^^^^^^^^^^^^^

This project utilizes Sphinx, a documentation generator in Python3.


Admonitions
~~~~~~~~~~~

At most times, admonitions are generated with the ``admonition`` directive instead, followed by the admonition title. Its class may vary on what it wants to portray, though not limited to:

- ``tip``: Additional useful information regarding that topic.

- ``hint``: Examples and alike.


Links
~~~~~

For a cleaner/readable source code, hyperlinks must be written in **reference** or **targeted form**. Its directives must be placed at the bottom-most part of the source code/file.

.. code-block:: rst

    This is a reference_. Works for `multiple words`_ too.

    .. _reference: https://google.com
    .. _multiple words: https://example.com