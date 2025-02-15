===================================
Rule ``long_to_shorthand_operator``
===================================

Shorthand notation for operators should be used if possible.

Warning
-------

Using this rule is risky
~~~~~~~~~~~~~~~~~~~~~~~~

Risky when applying for string offsets (e.g. ``<?php $text = "foo"; $text[0] =
$text[0] & "\x7F";``).

Examples
--------

Example #1
~~~~~~~~~~

.. code-block:: diff

   --- Original
   +++ New
    <?php
   -$i = $i + 10;
   +$i += 10;

Rule sets
---------

The rule is part of the following rule sets:

- `@PhpCsFixer:risky <./../../ruleSets/PhpCsFixerRisky.rst>`_
- `@Symfony:risky <./../../ruleSets/SymfonyRisky.rst>`_

Source class
------------

`PhpCsFixer\\Fixer\\Operator\\LongToShorthandOperatorFixer <./../src/Fixer/Operator/LongToShorthandOperatorFixer.php>`_
