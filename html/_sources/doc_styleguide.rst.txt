.. _doc_styleguide:

Documentation style guide
#########################

See Zephyr's `Documentation Guidelines <https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/zephyr/guides/documentation/index.html#doc-guidelines>`_  for a short introduction to RST and, most importantly, to the conventions used in Zephyr.
More information about RST is available in the `reStructuredText Primer <http://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_.

The documentation follows the Zephyr style guide, and adds a few more restrictive rules that are described below.

Titles and headings
*******************

Keep titles and headings as short and to the point as possible.

Titles
======

Mention the module name in the title and within the RST tag of the page, which is defined in the first line of the RST file.
For example:

.. code-block:: none

    1 .. _lib_aws_fota:
    2
    3 AWS FOTA
    4 ########

Do not repeat the section name in the titles of the subpages.
For example, when adding a sample or library, do not mention *sample* or *library* in the title of the page.

.. simple_title_table:

+-----------------------------+----------------------------------+
| Correct title               | Incorrect title                  |
+=============================+==================================+
| nRF9160: Secure Services    | nRF9160: Secure Services Sample  |
+-----------------------------+----------------------------------+
| DK Button and LED           | DK Button and LED library        |
+-----------------------------+----------------------------------+

Headings
========

Headings use sentence case, which means that the first word is capitalized, and the following words use normal capitalization.
The only exception are proper names, for example Bluetooth specification terminology (see last entry in the following table).

.. sentence_case_table:

+-----------------------------------------------------+---------------------------------------------------+
| Correct heading                                     | Incorrect heading                                 |
+=====================================================+===================================================+
| CC file format                                      | CC File Format                                    |
+-----------------------------------------------------+---------------------------------------------------+
| Sending shell commands                              | Sending Shell Commands                            |
+-----------------------------------------------------+---------------------------------------------------+
| GATT Human Interface Device (HID) Service Client    | GATT Human Interface Device (HID) service client  |
+-----------------------------------------------------+---------------------------------------------------+

Do not use consecutive headings without intervening text.

RST file formatting
*******************

For readability reasons, start every sentence on a new line in the source files and do not add line breaks within the sentence.
In the output, consecutive lines without blank lines in between are combined into one paragraph.

.. note:: For the conceptual documentation written in RST, you can have more than 80 characters per line.
          The requirement for 80 characters per line applies only to the code documentation written in doxygen.

The sentences must not end with a space.
Trim trailing spaces before committing your changes.

Each RST file must end with one blank line.

Content highlighting
********************

Use the following highlighing rules in the RST conceptual documentation:

.. content_highlighting_table:

+------------------------+------------------------+-----------------------------------------------------------------+
| Markup                 | Example                | Usage criteria                                                  |
+========================+========================+=================================================================+
| ``*emphasis*``         | *relaying*             | Emphasis or new terms.                                          |
+------------------------+------------------------+-----------------------------------------------------------------+
| ````code````           | ``west update``        | Code within text.                                               |
+------------------------+------------------------+-----------------------------------------------------------------+
| ``**PCB**``            | **SW3**                | PCB names.                                                      |
+------------------------+------------------------+-----------------------------------------------------------------+
| ``:guilabel:`GUI```    | :guilabel:`Cancel`     | Clickable graphical user interface elements.                    |
+------------------------+------------------------+-----------------------------------------------------------------+
| ``:file:`filename```   | :file:`conf.py`        | Filenames, file paths, directory names, and file extensions.    |
+------------------------+------------------------+-----------------------------------------------------------------+

.. note:: Do not use the following markup for italics: ```..```.

For readability reasons, do not use any code highlighting for titles of other pages or headings when they are mentioned in the text.
For example, do not write "The ``bl_crypto`` library".
Use the complete name of the library: "The bootloader crypto library", and always link to the page you mention.
If the page you are linking to is mentioned several times in the text, place the link on the first occurrence and on every occurrence where linking to the page is useful.

Tables
******

Follow Zephyr's `Documentation Guidelines <https://developer.nordicsemi.com/nRF_Connect_SDK/doc/latest/zephyr/guides/documentation/index.html#doc-guidelines>`_ for tables.
Do not add table titles to describe the table.
Instead, make sure to introduce the table with a short sentence that describes the table contents.
For example:

.. code-block:: none

    The following table lists something.

    .. list-table::
        :widths: 15 20 40
        :header-rows: 1

        * - Heading 1
          - Heading 2
          - Heading 3
        * - body row 1, column 1
          - body row 1, column 2
          - body row 1, column 3
