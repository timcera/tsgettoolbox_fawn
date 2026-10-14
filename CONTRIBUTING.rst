============
Contributing
============
Contributions are welcome, and they are greatly appreciated! Every
little bit helps, and credit will always be given.

You can contribute in many ways:

Types of Contributions
----------------------

Report Bugs
~~~~~~~~~~~
Report bugs at https://github.com/timcera/tsgettoolbox_fawn

If you are reporting a bug, please include:

* Your operating system name and version.
* Any details about your local setup that might be helpful in troubleshooting.
* Detailed steps to reproduce the bug.

Fix Bugs
~~~~~~~~
Look through the github issues for bugs. Anything tagged with "bug" is open to
whoever wants to implement it.

Implement Features
~~~~~~~~~~~~~~~~~~
Look through the github issues for features. Anything tagged with "feature" is
open to whoever wants to implement it.

Write Documentation
~~~~~~~~~~~~~~~~~~~
tsgettoolbox_fawn could always use more documentation, whether as part of the
official tsgettoolbox_fawn docs or in docstrings.

Submit Feedback
~~~~~~~~~~~~~~~
The best way to send feedback is to file an issue at
https://github.com/timcera/tsgettoolbox_fawn

If you are proposing a feature:

* Explain in detail how it would work.
* Keep the scope as narrow as possible, to make it easier to implement.
* Remember that this is a volunteer-driven project, and that contributions
  are welcome :)

Get Started!
------------
Ready to contribute? Here's how to set up `tsgettoolbox_fawn` for local development.

1. Fork the `tsgettoolbox_fawn` repo at
   https://github.com/timcera/tsgettoolbox_fawn

2. Clone your fork locally::

    $ git clone git@github.com:your_github_login/tsgettoolbox_fawn.git

3. Create a virtual python environment with `pip` or `conda` (whatever you
   prefer) and activate it, and install `tsgettoolbox_fawn` in development
   mode::

    #     Using conda would be something like this:
    $ conda create -n tsgettoolbox_fawn python=3.11
    $ conda activate tsgettoolbox_fawn
    $ cd tsgettoolbox_fawn/

    #     The following command will list all the dependencies that will be
    #     installed, but not actually install them.
    $ python -m pip install --dry-run -e .

    #     Use conda to install the dependencies listed above, excluding
    #     tsgettoolbox_fawn itself. For example:
    $ conda install -c conda-forge numpy pandas

    #     Now install tsgettoolbox_fawn in development mode.
    $ python -m pip install -e .

4. For linting, reformatting, and testing you also need to install ruff and
   pytest::

    $ conda install -c conda-forge ruff pytest

5. Create a branch for local development::

    $ git checkout -b name-of-your-bugfix-or-feature

    Now you can make your changes locally.

6. When you're done making changes, check that your changes pass pytest, the
   ruff linter and ruff formatter.::

    $ ruff check -f --select "I" .
    $ ruff format .
    $ pytest

7. Commit your changes and push your branch to github::

    $ git add .  # or choose the specific files you want to add
    $ git commit -m "Your detailed description of your changes."
    $ git push origin name-of-your-bugfix-or-feature

8. Submit a pull request through the github website.

Pull Request Guidelines
-----------------------

Before you submit a pull request, check that it meets these guidelines:

1. The pull request should include tests.
2. If the pull request adds functionality, the docs should be updated. Put
   your new functionality into a function with a docstring, and add the
   feature to the list in README.rst.
3. The pull request should work for Python 3.10 and above.
