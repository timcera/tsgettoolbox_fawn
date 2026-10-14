.. image:: https://img.shields.io/coveralls/github/timcera/tsgettoolbox_fawn
    :alt: Test Coverage
    :target: https://coveralls.io/r/timcera/tsgettoolbox_fawn?branch=master
    :height: 20

.. image:: https://img.shields.io/pypi/v/tsgettoolbox_fawn
    :alt: Latest release
    :target: https://pypi.python.org/pypi/tsgettoolbox_fawn/
    :height: 20

.. image:: https://img.shields.io/pypi/l/tsgettoolbox_fawn
    :alt: BSD-3 clause license
    :target: https://pypi.python.org/pypi/tsgettoolbox_fawn/
    :height: 20

.. image:: https://img.shields.io/pypi/pyversions/tsgettoolbox_fawn
    :alt: PyPI - Python Version
    :target: https://pypi.org/project/tsgettoolbox_fawn/
    :height: 20

tsgettoolbox_fawn - Quick Guide
===============================
The 'tsgettoolbox_fawn' is a plugin-in for 'tsgettoolbox' that supplies
a command line interface and Python library to get time-series data from the
Florida Automated Weather Network (FAWN) The tsgettoolbox_fawn will work with
Python 3.10+.

Documentation
-------------
Reference documentation is at `tsgettoolbox FAWN API`_.

Installation
------------
At the command line::

    $ pip install tsgettoolbox_fawn

    OR

    $ conda install -c conda-forge tsgettoolbox_fawn

Usage Summary - Command Line
----------------------------
Just run 'tsgettoolbox --help' to get a list of subcommands.  To get detailed
help for a particular sub-command, for instance 'fawn', type 'tsgettoolbox
fawn --help'.

+-------------+---------+--------+---------+----------+-----------------------+
| Sub-command | Spatial | Time   | Type    | Time     | Description           |
|             | Extent  | Extent |         | Interval |                       |
+=============+=========+========+=========+==========+=======================+
| fawn        | US/FL   | varies | station | 15T,H,D, | Florida Automated     |
|             |         |        |         | M        | Weather               |
+-------------+---------+--------+---------+----------+-----------------------+

+-------------------+-------------+
| Time Interval     | Description |
| Code              |             |
+===================+=============+
| T                 | Minute      |
+-------------------+-------------+
| H                 | Hourly      |
+-------------------+-------------+
| D                 | Daily       |
+-------------------+-------------+
| M                 | Monthly     |
+-------------------+-------------+

Usage Summary - Python Library
------------------------------
To use the tsgettoolbox in a project::

    from tsgettoolbox import tsgettoolbox
    df = tsgettoolbox.fawn(
        stations=["Alachua" ,120"],
        variables=["rainfall" ,"winddir"],
        reportType="all",
        start_date="2019-01-01",
        end_date="2020-01-01",
    )
    print(df.head())

Refer to the API Documentation at `tsgettoolbox FAWN API`_.

Usage Summary - Command Line
----------------------------

    tsgettoolbox fawn \
        --stations="Alachua,120" \
        --variables="rainfall,winddir" \
        --reportType="all" \
        --start_date="2019-01-01" \
        --end_date="2020-01-01" > output.csv

Refer to the command line documentation at `tsgettoolbox FAWN CLI`_.

Development
~~~~~~~~~~~
Development is managed on bitbucket or github.
https://bitbucket.org/timcera/tsgettoolbox_fawn/overview.
https://github.com/timcera/tsgettoolbox_fawn

.. _tsgettoolbox_documentation: https://timcera.bitbucket.io/tsgettoolbox/docs/index.html#tsgettoolbox-documentation_fawn
.. _tsgettoolbox FAWN API: https://timcera.bitbucket.io/tsgettoolbox/docs/function_summary.html
.. _tsgettoolbox FAWN CLI: https://timcera.bitbucket.io/linked_pkg_dirs/tsgettoolbox/docs/command_line.html#fawn
