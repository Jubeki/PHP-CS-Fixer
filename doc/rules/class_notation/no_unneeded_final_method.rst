=================================
Rule ``no_unneeded_final_method``
=================================

Removes ``final`` from methods where possible.

Warning
-------

Using this rule is risky
~~~~~~~~~~~~~~~~~~~~~~~~

Risky when child class overrides a ``private`` method.

Configuration
-------------

``private_methods``
~~~~~~~~~~~~~~~~~~~

Private methods of non-``final`` classes must not be declared ``final``.

Allowed types: ``bool``

Default value: ``true``

Examples
--------

Example #1
~~~~~~~~~~

*Default* configuration.

.. code-block:: diff

   --- Original
   +++ New
    <?php
    final class Foo
    {
   -    final public function foo1() {}
   -    final protected function bar() {}
   -    final private function baz() {}
   +    public function foo1() {}
   +    protected function bar() {}
   +    private function baz() {}
    }

    class Bar
    {
   -    final private function bar1() {}
   +    private function bar1() {}
    }

Example #2
~~~~~~~~~~

With configuration: ``['private_methods' => false]``.

.. code-block:: diff

   --- Original
   +++ New
    <?php
    final class Foo
    {
   -    final private function baz() {}
   +    private function baz() {}
    }

    class Bar
    {
        final private function bar1() {}
    }

Rule sets
---------

The rule is part of the following rule sets:

- `@PHP80Migration:risky <./../../ruleSets/PHP80MigrationRisky.rst>`_
- `@PhpCsFixer:risky <./../../ruleSets/PhpCsFixerRisky.rst>`_
- `@Symfony:risky <./../../ruleSets/SymfonyRisky.rst>`_

Source class
------------

`PhpCsFixer\\Fixer\\ClassNotation\\NoUnneededFinalMethodFixer <./../src/Fixer/ClassNotation/NoUnneededFinalMethodFixer.php>`_
