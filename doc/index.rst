|test|_

About
=====

Various string utilities in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-string

String builder example
======================

A basic example that creates a string from numbers and strings.

.. code-block:: python

   from string import StringBuilder

   def main():
       builder = StringBuilder()
       builder += "Temperature: "
       builder += 5
       builder += 'C'

       assert builder.to_string() == "Temperature: 5 C"

String reader example
=====================

A basic example that uses the string reader class to get characters
from a string.

.. code-block:: python

   from string import StringReader

   def main():
       reader = StringReader("kalle kula")
       assert reader.peek() == 'k'
       assert reader.get() == 'k'
       assert reader.get() == 'a'
       assert reader.read(3) == "lle"
       assert reader.get() == ' '
       assert reader.read() == "kula"
       assert reader.get() == ''
       assert reader.peek() == ''
       assert reader.read() == ""
       assert reader.read(100) == ""
       reader.unget()
       assert reader.available() == 1
       assert reader.get() == 'a'
       assert reader.get() == ''

Functions and types
===================

.. mysfile:: src/lib.mys

.. |test| image:: https://github.com/mys-lang/package-string/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-string/actions/workflows/pythonpackage.yml

.. _Mys programming language: https://mys-lang.org
