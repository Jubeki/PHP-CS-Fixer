=================================
Rule ``switch_continue_to_break``
=================================

Switch case must not be ended with ``continue`` but with ``break``.

Examples
--------

Example #1
~~~~~~~~~~

.. code-block:: diff

   --- Original
   +++ New
    <?php
    switch ($foo) {
        case 1:
   -        continue;
   +        break;
    }

Example #2
~~~~~~~~~~

.. code-block:: diff

   --- Original
   +++ New
    <?php
    switch ($foo) {
        case 1:
            while($bar) {
                do {
   -                continue 3;
   +                break 3;
                } while(false);

                if ($foo + 1 > 3) {
                    continue;
                }

   -            continue 2;
   +            break 2;
            }
    }

Rule sets
---------

The rule is part of the following rule sets:

- `@PhpCsFixer <./../../ruleSets/PhpCsFixer.rst>`_
- `@Symfony <./../../ruleSets/Symfony.rst>`_

Source class
------------

`PhpCsFixer\\Fixer\\ControlStructure\\SwitchContinueToBreakFixer <./../src/Fixer/ControlStructure/SwitchContinueToBreakFixer.php>`_
