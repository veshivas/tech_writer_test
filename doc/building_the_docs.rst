.. _building_the_docs:

Building the documentation
##########################

Before you can build the documentation, you must install `Sphinx <https://www.sphinx-doc.org/>`_.
See the `installation instructions <https://www.sphinx-doc.org/en/master/usage/installation.html>`_ on the Sphinx website for detailed information.

To build the documentation, complete the following steps:

1. Open a command window in the :file:`doc` folder.
#. Enter ``make html`` to build the HTML output.

   .. tip::
      If you get an error message that the **make** command cannot be found, you might be in the wrong folder, or you might need to explicitly state which command to run (for example, ``./make.bat html`` on Windows).

      On Linux, you might need to install **make** as instructed.

The documentation build reports any errors or warnings that occur.
The output is placed in the ``doc/_build/html`` folder.
Open ``doc/_build/html/index.html`` to start browsing the documentation.
