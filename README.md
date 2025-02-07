[![pdocs - Documentation Powered by Your Python Code.](https://raw.github.com/timothycrosley/pdocs/master/art/logo_large.png)](https://timothycrosley.github.io/pdocs/)
_________________

[![PyPI version](https://badge.fury.io/py/pdocs.svg)](http://badge.fury.io/py/pdocs)
[![Build Status](https://travis-ci.org/timothycrosley/pdocs.svg?branch=master)](https://travis-ci.org/timothycrosley/pdocs)
[![codecov](https://codecov.io/gh/timothycrosley/pdocs/branch/master/graph/badge.svg)](https://codecov.io/gh/timothycrosley/pdocs)
[![Join the chat at https://gitter.im/pdocs/community](https://badges.gitter.im/pdocs/community.svg)](https://gitter.im/pdocs/community?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![License](https://img.shields.io/github/license/mashape/apistatus.svg)](https://pypi.python.org/pypi/pdocs/)
[![Downloads](https://pepy.tech/badge/pdocs)](https://pepy.tech/project/pdocs)
_________________

[Read Latest Documentation](https://timothycrosley.github.io/pdocs/) - [Browse GitHub Code Repository](https://github.com/timothycrosley/pdocs/)
_________________


`pdocs` is a library and a command line program to discover the public
interface of a Python module or package. The `pdocs` script can be used to
generate Markdown or HTML of a module's public interface, or it can be used
to run an HTTP server that serves generated HTML for installed modules.

`pdocs` is an MIT Licensed fork of `pdoc` with the goal of staying true to the original vision
layed out by the projects creator.

NOTE: For most projects, the best way to use `pdocs` is using [portray](https://timothycrosley.github.io/portray/).

[![asciicast](https://asciinema.org/a/265744.svg)](https://asciinema.org/a/265744)

Features
--------

* Support for documenting data representation by traversing the abstract syntax
  to find docstrings for module, class and instance variables.
* For cases where docstrings aren't appropriate (like a
  [namedtuple](http://docs.python.org/2.7/library/collections.html#namedtuple-factory-function-for-tuples-with-named-fields)),
  the special variable `__pdocs__` can be used in your module to
  document any identifier in your public interface.
* Usage is simple. Just write your documentation as Markdown. There are no
  added special syntax rules.
* `pdocs` respects your `__all__` variable when present.
* `pdocs` will automatically link identifiers in your docstrings to its
  corresponding documentation.
* When `pdocs` is run as an HTTP server, external linking is supported between
  packages.
* The `pdocs` HTTP server will cache generated documentation and automatically
  regenerate it if the source code has been updated.
* When available, source code for modules, functions and classes can be viewed
  in the HTML documentation.
* Inheritance is used when possible to infer docstrings for class members.

The above features are explained in more detail in pdocs's documentation.

`pdocs` is compatible with Python 3.6 and newer.

## Quick Start

The following guides should get you up using pdocs in no time:

1. [Installation](https://timothycrosley.github.io/pdocs/docs/quick_start/1.-installation/) - TL;DR: Run `pip3 install pdocs` within your projects virtual environment.
2. [Command Line Usage](https://timothycrosley.github.io/pdocs/docs/quick_start/2.-cli/) - TL;DR: Run `pdocs server YOUR_MODULES` to test and `pdocs as_html YOUR_MODULES` to generate HTML.
3. [API Usage](https://timothycrosley.github.io/pdocs/docs/quick_start/3.-api/) - TL;DR: Everything available via the CLI is also easily available programmatically from within Python.

## Why Create `pdocs`?

I created `pdocs` to help power [portray](https://timothycrosley.github.io/portray/) while staying true to the original vision of `pdoc` and maintain
MIT license compatibility. In the end I created it to help power better documentation websites for Python projects.

I hope you too find `pdocs` useful!

~Timothy Crosley
