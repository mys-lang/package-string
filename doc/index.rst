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

Functions and types
===================

.. mysfile:: src/lib.mys

.. _Mys programming language: https://mys.readthedocs.io/en/latest/
