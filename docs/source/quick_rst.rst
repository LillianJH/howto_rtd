.. quick_rst:

Quick Start Guide to reStructured Text
=======================================

This is a quick start guide to reStructured Text syntax for new users.

If you're trying to do something that isn't covered by this guide, there is extensive documetnation available here: 

.. contents:: 
    :local:
    :backlinks: entry
    :depth: 2

Headings
-----------

The document title and headings are created using non-alphanumeric 7-bit ASCII characters (i.e. "= - ` : ' " ~ ^ _ * + # < >"). Underline each heading (under- and over-line the title) with the chosen character, ensuring the line is at least as long as the heading, or title. Below is an example of the title and headings inputs used in this document.

.. code-block:: rst
 
    ======================================
    Getting Started with reStructuredText
    ======================================
    1. Purpose
    ----------
    2. Headings
    -----------
    ...
    5. Lists
    ---------
    5.1. Bullet Lists
    ##################

Paragraphs
--------------

Paragraphs are created by separating text with blank lines, see the example below.

Input:

.. code-block:: rst

    This is a paragraph
    
    This is another paragraph
    
    And this is another paragraph
    
Output:

This is a paragraph

This is another paragraph

And this is another paragraph

Inline markups
------------------
Bold
~~~~~~~~~~

To make a word or phrase display in boldface, surround the word or phrase in double asterisks.

Input:

.. code-block:: rst

    This is an example of **boldface**

Output:

This is an example of **boldface**

Italics
~~~~~~~~

To make a word or phrase display in italics, surround the word or phrase in single asterisks.

Input:

.. code-block:: rst

    This is an example of *italics*

Output:

This is an example of *italics*

Hyperlinks
~~~~~~~~~~~~~~

External Targets
^^^^^^^^^^^^^^^^^^^^^

For single word hyperlinks to external targets, insert an underscore after the word and define the target, on a separate line, as shown in the example below.

.. code-block:: rst
    
    External hyperlink example with Google_.
    
    .. _Google: https://urldefense.com/v3/__https://www.Google.com__;!!DZ3fjg!8xAtY03iF7viV8Npa1mY6S8-PGymyJfqvv7pXr6i0waiTMC95a1G8qeFb2gaHkBKvZJUCFu_SVW4Us4nnxA$ 
    
External hyperlink example with Google_.
 
.. _Google: https://urldefense.com/v3/__https://www.Google.com__;!!DZ3fjg!8xAtY03iF7viV8Npa1mY6S8-PGymyJfqvv7pXr6i0waiTMC95a1G8qeFb2gaHkBKvZJUCFu_SVW4Us4nnxA$ 

For hyperlinks that include spacing or punctuation, surround the phrase with backticks (`) prior to appending the underscore.

.. code-block:: rst
 
    This `links to Wikipedia`_.
    
    .. _links to Wikipedia: https://urldefense.com/v3/__https://en.wikipedia.org__;!!DZ3fjg!8xAtY03iF7viV8Npa1mY6S8-PGymyJfqvv7pXr6i0waiTMC95a1G8qeFb2gaHkBKvZJUCFu_SVW4iN6OpJ8$ 

This `links to Wikipedia`_.

.. _links to Wikipedia: https://urldefense.com/v3/__https://en.wikipedia.org__;!!DZ3fjg!8xAtY03iF7viV8Npa1mY6S8-PGymyJfqvv7pXr6i0waiTMC95a1G8qeFb2gaHkBKvZJUCFu_SVW4iN6OpJ8$ 

Internal Targets
^^^^^^^^^^^^^^^^^^^^^

To create hyperlinks to sections within the document, precede the heading name with an underscore; if the heading has spacing or punctuation, surround it with backticks (`).

.. code-block:: rst

    This links to the `1. Purpose`_ section.
    
This links to the `1. Purpose`_ section.

To link to a section within the document without matching the heading name in the text, create an internal hyperlink as shown in the example below.

.. code-block:: rst
    
    In the next paragraph 'here' will link to the Purpose section.
    
    See `here <#purpose>`_
    
In the next paragraph 'here' will link to the Purpose section.

See `here <#purpose>`_

Lists
---------

Bullet Lists
~~~~~~~~~~~~~~

Bullet lists can be created using '-', '*', or '+'. Note, there must be a blank line inserted before the first item in the list and after the last item.

Input:

.. code-block:: rst
    
    This is a bullet list:
    
    - This is the first bullet
    - This is the second bullet
    - This is the last bullet

Output:

This is a bullet list:

- This is the first bullet
- This is the second bullet
- This is the last bullet

Numbered Lists
~~~~~~~~~~~~~~~~

Numbered lists can be created by manually numbering each item (1., 2., etc.) or through automatic numbering using '#.' Note, there must be a blank line inserted before the first item in the list and after the last item.

Input:

.. code-block:: rst

    This is a numbered list:
    
    1. One is the first number on the list
    #. This number was auto-generated
    #. This number was also auto-generated and is the last number on the list

Output:

This is a numbered list:

1. One is the first number on the list
#. This number was auto-generated
#. This number was also auto-generated and is the last number on the list

Tables
----------

Simple Table
~~~~~~~~~~~~~

Simple tables use '=' and '-' to define the heading(s), rows, and columns as shown in the example below. Simple tables are simple to create, but have limitations on row and column spanning.

Input:

.. code-block:: rst

    === === ===
    Addends Sum
    ------- ---
     a   b  a+b
    === === ===
     1   2   3
     5   6   11
     4   2   6
    === === ===

Output:

=== === ===
Addends Sum
------- ---
 a   b  a+b
=== === ===
 1   2   3
 5   6   11
 4   2   6
=== === ===

Grid Table
~~~~~~~~~~~~~~

Grid tables are created using '-' for row delineators, '+' for corner delineators, and '|' for column delineators. Grid table are more cumbersome to create, but offer more flexibility in row and column spanning. 

Input:

.. code-block:: rst

    +------------+------------+-----------+
    |     Header of the Addition Table    |
    +============+============+===========+
    |         Addends         |    Sum    |
    +------------+------------+-----------+
    |     2      |            |     7     |
    +------------+     5      +-----------+
    |     4      |            |     9     |
    +------------+------------+-----------+
    |     6      |     7      |     13    |
    +------------+------------+-----------+

Output:

+------------+------------+-----------+
|     Header of the Addition Table    |
+============+============+===========+
|         Addends         |    Sum    |
+------------+------------+-----------+
|     2      |            |     7     |
+------------+     5      +-----------+
|     4      |            |     9     |
+------------+------------+-----------+
|     6      |     7      |     13    |
+------------+------------+-----------+

Comments
------------

Comments can be inserted by adding '..' at the beginning of the line. Comments only show in the .rst code an are not rendered into the document.

Input:

.. code-block:: rst

    .. This is a comment and won't be rendered

Output: (not rendered)

.. This is a comment and won't be rendered

Images
----------

Images can be inserted using '.. image::' or '.. figure::'. A figure is an image with a caption.

Input:

.. code-block:: rst
    
    .. image:: theimage.jpeg
    
    .. figure:: thefigure.jpeg
    
    This is the caption for the figure

Footnotes
--------------

Similar to lists, footnotes can be manually or automatically numbered. In either case, the number, or '#', is surrounded by brackets ('[' and ']'), and appended with an underscore'_' as shown in the example below.

Input:

.. code-block:: rst
    
    There is an example of a footnote [1]_ in this sentence.
    
    Footnotes can also be auto-numerated using the # similar to numbered lists [#]_.
    
    .. [1] this is what the footnote is tied to
    
    .. [#] this is what the other footnote is tied to

Output (see bottom of page for footnotes):

There is an example of a footnote [1]_ in this sentence.

Footnotes can also be auto-numerated using the # similar to lists [#]_.

References
---------------

10.1 https://urldefense.com/v3/__https://docutils.sourceforge.io/rst.html__;!!DZ3fjg!8xAtY03iF7viV8Npa1mY6S8-PGymyJfqvv7pXr6i0waiTMC95a1G8qeFb2gaHkBKvZJUCFu_SVW4gzUeuEY$ 

10.2 https://urldefense.com/v3/__https://en.wikipedia.org__;!!DZ3fjg!8xAtY03iF7viV8Npa1mY6S8-PGymyJfqvv7pXr6i0waiTMC95a1G8qeFb2gaHkBKvZJUCFu_SVW4iN6OpJ8$ 

.. [1] this is what the footnote is tied to

.. [#] this is what the other footnote is tied to
