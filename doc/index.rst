|discord|_
|test|_
|stars|_

About
=====

Various string utilities in the `Mys programming language`_.

Project: https://github.com/mys-lang/package-string

String builder example
======================

A basic example that creates a string from numbers and strings.

.. code-block:: mys

   from string import StringBuilder

   func main():
       builder = StringBuilder()
       builder += "Temperature: "
       builder += 5
       builder += 'C'

       assert builder.to_string() == "Temperature: 5 C"

String reader example
=====================

A basic example that uses the string reader class to get characters
from a string.

.. code-block:: mys

   from string import StringReader

   func main():
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

API
===

.. mysfile:: src/lib.mys

.. |discord| image:: https://img.shields.io/discord/777073391320170507?label=Discord&logo=discord&logoColor=white
.. _discord: https://discord.gg/GFDN7JvWKS

.. |test| image:: https://github.com/mys-lang/package-string/actions/workflows/pythonpackage.yml/badge.svg
.. _test: https://github.com/mys-lang/package-string/actions/workflows/pythonpackage.yml

.. |stars| image:: https://img.shields.io/github/stars/mys-lang/package-string?style=social
.. _stars: https://github.com/mys-lang/package-string

.. _Mys programming language: https://mys-lang.org
