=======================================
Rule ``no_trailing_comma_in_list_call``
=======================================

Remove trailing commas in list function calls.

Warning
-------

This rule is deprecated and will be removed in the next major version
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You should use ``no_trailing_comma_in_singleline`` instead.

Examples
--------

Example #1
~~~~~~~~~~

.. code-block:: diff

   --- Original
   +++ New
    <?php
   -list($a, $b,) = foo();
   +list($a, $b) = foo();
Source class
------------

`PhpCsFixer\\Fixer\\ControlStructure\\NoTrailingCommaInListCallFixer <./../src/Fixer/ControlStructure/NoTrailingCommaInListCallFixer.php>`_
