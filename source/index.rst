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

.. toctree::
    :maxdepth: 1
    :caption: Cloudflare

    Introductory <./cloudflare/index.rst>
    cloudflare/workers/index

.. toctree::
    :maxdepth: 1
    :caption: Computers
    
    Introductory <./computers/index.rst>
    computers/history_of_computing

.. toctree::
    :maxdepth: 1
    :caption: Computer Programming
    
    Introductory <./programming/index.rst>
    programming/editors
    programming/databases/index
    programming/languages/index

.. toctree::
    :maxdepth: 1
    :caption: Database Management Systems

    Introductory <./dbms/index.rst>

.. toctree::
    :maxdepth: 1
    :caption: Data Structures & Algorithms
    
    Introductory <./dsa/index.rst>
    dsa/algorithms/index
    dsa/data_structures/index
    dsa/space_complexity
    dsa/time_complexity

.. toctree::
    :maxdepth: 1
    :caption: Discord

    Introductory <./discord/index.rst>
    discord/api/index
    discord/markdown
    discord/message_formatting

.. toctree::
    :maxdepth: 1
    :caption: Discrete Mathematics
    
    Introductory <./discrete_mathematics/index.rst>
    discrete_mathematics/functions/index
    discrete_mathematics/graph_theory/index
    discrete_mathematics/integers_and_divisibility
    discrete_mathematics/matrix
    discrete_mathematics/number_systems
    discrete_mathematics/probability_theory/index
    discrete_mathematics/propositions/index
    discrete_mathematics/set_theory

.. toctree::
    :maxdepth: 1
    :caption: Graphics and Visual Computing

    Introductory <./graphics_and_visual_computing/index.rst>
    graphics_and_visual_computing/foundations
    graphics_and_visual_computing/design_principles
    graphics_and_visual_computing/graphics_programming
    graphics_and_visual_computing/animation_and_interaction

.. toctree::
    :maxdepth: 1
    :caption: Information Management

    Introductory <./information_management/index.rst>
    information_management/fundamentals
    information_management/erd
    information_management/reengineering_of_databases
    information_management/uml
    information_management/database_normalization
    information_management/mysql
    information_management/db_administration
    information_management/distributed_db
    information_management/data_distribution

.. toctree::
    :maxdepth: 1
    :caption: IS Innovations

    Introductory <./is_innovations/index.rst>
    is_innovations/disruptive_innovation
    is_innovations/iot

.. toctree::
    :maxdepth: 1
    :caption: Web Development

    Introductory <./webdev/index.rst>
    webdev/canvas/index
    webdev/resources


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