.. _`PyPA Roadmap`:

===================
PyPA Specifications
===================

In addition to maintaining the default implementation of the Python packaging
toolchain, the Python Packaging Authority is also responsible for maintaining
the interoperability specifications used to define the interactions between
those tools.

Specification Process
---------------------

PyPA interoperability specifications are currently handled as Informational
Python Enhancement Proposals in accordance with :pep:`1`.

Whenever a new PEP is put forward on distutils-sig, any PyPA core
reviewer that believes they are suitably experienced to make the final
decision on that PEP may offer to serve as the BDFL's delegate (or
"PEP czar") for that PEP. If their self-nomination is accepted by the
other PyPA core reviewer, the lead PyPI maintainer and the lead
CPython representative on distutils-sig, then they will have the
authority to approve (or reject) that PEP.

The current lead PyPI maintainer is Donald Stufft, while the current lead
CPython representative on distutils-sig is Nick Coghlan.


Active Specifications
---------------------

Core metadata
~~~~~~~~~~~~~

The current core metadata file format, version 1.2, is specified in :pep:`345`.

However, the version specifiers and environment markers sections of that PEP
have been superceded as described below. In addition, metadata files are
permitted to contain the following additional field:

Provides-Extra (multiple use)
:::::::::::::::::::::::::::::

A string containing the name of an optional feature. Must be a valid Python
identifier. May be used to make a dependency conditional on whether the
optional feature has been requested.

Example::

    Provides-Extra: pdf
    Requires-Dist: reportlab; extra == 'pdf'

A second distribution requires an optional dependency by placing it
inside square brackets, and can request multiple features by separating
them with a comma (,). The requirements are evaluated for each requested
feature and added to the set of requirements for the distribution.

Example::

    Requires-Dist: beaglevote[pdf]
    Requires-Dist: libexample[test, doc]

Two feature names `test` and `doc` are reserved to mark dependencies that
are needed for running automated tests and generating documentation,
respectively.

It is legal to specify ``Provides-Extra:`` without referencing it in any
``Requires-Dist:``.

Version Specifiers
~~~~~~~~~~~~~~~~~~

Version numbering requirements and the semantics for specifying comparisons
between versions are definined :pep:`440`.

The version specifiers section in this PEP supersedes the version specifiers
section in :pep:`345`.

Dependency Specifiers
~~~~~~~~~~~~~~~~~~~~~

The dependency specifier format used to declare a dependency on another
component is defined in :pep:`508`.

The environment markers section in this PEP supersedes the environment markers
section in :pep:`345`.

Source Distribution Format
~~~~~~~~~~~~~~~~~~~~~~~~~~

The source distribution format (``sdist``) is not currently formally defined.
Instead, it's format is implicitly defined by the behaviour of the
standard library's ``distutils`` module when executing the ``setup.py sdist``
command.

Binary Distribution Format
~~~~~~~~~~~~~~~~~~~~~~~~~~

The binary distribution format (``wheel``) is defined in :pep:`427`.

Platform Compatibility Tags
~~~~~~~~~~~~~~~~~~~~~~~~~~~

The platform compatibility tagging model used for ``wheel`` distribution is
defined in :pep:`425`.

Recording Installed Distributions
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The format used to record installed packages and their contents is defined in
:pep:`376`.

Note that only the ``dist-info`` directory and the ``RECORD`` file format from
that PEP are currently implemented in the default packaging toolchain.
