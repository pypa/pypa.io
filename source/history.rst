.. _`History`:

=================
Packaging History
=================

2021
----

* `The PyPA became a PSF Fiscal Sponsoree`_


2020
----

* `Old pypa-dev Google Group decommissioned`_ to focus conversation
  in Discourse forum and distutils-sig list.
* `Packaging Working Group used MOSS and CZI funding to improve pip
  dependency resolver`_.
* :pep:`609` created and accepted, creating PyPA governance model.
* `New pip dependency resolver released`_.

2019
----

* `OTF grant for PyPI awarded to PSF`_, team worked on security,
  localization, and accessibility improvements to Warehouse.

2018
----

* Warehouse `superseded and replaced legacy PyPI
  <https://mail.python.org/mm3/archives/list/distutils-sig@python.org/thread/YREMU56QKRMTTFBFVFJ2B4EHOEKOJZFJ/>`_.
* Warehouse installation at pypi.org `entered beta phase
  <https://mail.python.org/pipermail/python-announce-list/2018-March/011883.html>`_.
* :pep:`566` accepted, adding better package metadata.

2017
----

* ``pipenv``-based application dependency management tutorial `added
  to PyPUG
  <https://github.com/pypa/python-packaging-user-guide/pull/369>`_.
* `MOSS grant for PyPI`_ awarded to PSF, team began in December to
  focus on replacing legacy PyPI.
* :pep:`517` accepted (``setup.py``-independent build system backends).
* Legacy pypi.python.org upload API `switched off
  <https://mail.python.org/pipermail/distutils-sig/2017-July/030849.html>`_.

2016
----

* :ref:`pip` version 9 (`pip release notes`_) started respecting the
  ``Requires-Python metadata`` field.
* Package uploads `started defaulting to pypi.org
  <https://mail.python.org/pipermail/distutils-sig/2017-June/030766.html>`_.
* pypi.org `deployed
  <https://mail.python.org/pipermail/distutils-sig/2016-August/029355.html>`_
  as a soft-launch with core functionality.
* :pep:`518` accepted (defining the ``pyproject.toml`` format for static
  build dependency declarations)
* PSF `hired an infrastructure manager
  <https://pyfound.blogspot.com.au/2016/04/the-psf-has-hired-it-manager.html>`_.
* :ref:`pip` v8.1 added ``manylinux1`` support (:pep:`513`, `pip
  release notes`_), PyPI starts allowing Linux wheel files
* :pep:`513` accepted (defining the ``manylinux1`` platform ABI).
* Version 8 of :ref:`pip` (`pip release notes`_) integrated artifact hash checking
  (previously dependent on the third-party project `peep`_).

2015
----

* :ref:`pip` (v7) started caching built :term:`wheels <pypug:Wheel>`, and
  installing from them, instead of installing directly from :term:`sdists
  <pypug:Source Distribution (or "sdist")>` (`pip release notes`_).
* :ref:`pip` (v7) started supporting ``--install-option`` and
  ``--global-option`` per requirement in requirement files (`pip release notes`_).
* :ref:`setuptools` (v18.3) now allows disabling of the manipulation of the
  sys.path during the processing of the easy-install.pth file.
* :pep:`470`, which deprecated external, non-PyPI hosting, was
  accepted.
* :pep:`503` published to standardise the PyPI simple repository API.
* :pep:`508` published to standardise the specification format for individual dependencies.

2014
----


* :ref:`pypug:setuptools` v8.0 and :ref:`pypug:pip` v6.0 (`pip release
  notes`_) implemented :pep:`440` (Python's new versioning scheme).
  Both projects now depend on the project :ref:`pypug:packaging` for
  this support.
* :pep:`477` backported :pep:`453` into Python 2.7.9.
* :pep:`453`: Being able to bootstrap ``pip`` into Python 3.4.
* https://bugs.python.org/issue19407: Modern Installation and Packaging guides on
  python.org.
* :ref:`virtualenv` (v1.11) started installing pip & setuptools using wheels.
* :ref:`pip` (v1.5.1) became available as a cross platform wheel on
  PyPI (`pip release notes`_).
* :ref:`pip` (v1.5.1) stop requiring :ref:`setuptools` to install
  wheels (`pip release notes`_).
* ``get-pip.py`` doesn't require setuptools to be installed first
* ``get-pip.py`` installs setuptools for you, if you don't already have it
* :pep:`449`: Removal of the DNS-based mirror autodiscovery
* `Refactored the pip docs <https://github.com/pypa/pip/pull/1556>`_ to be
  consistent with the `"PyPA Standard Docs Template"
  <https://gist.github.com/qwcode/8431828>`_
* PyPUG moved to the packaging.python.org subdomain.
* :pep:`440` published to standardise version descriptions and filtering.

2013
----

* :ref:`distlib` started releasing to PyPI, and :ref:`pip` began
  depending on it (`pip release notes`_).
* Core PyPI infrastructure relocated to OSU/OSL (with significantly
  increased resources)
* The core packaging projects were collected under the :term:`pypug:Python Packaging
  Authority (PyPA)` accounts on `GitHub <https://github.com/pypa>`_ and `Bitbucket
  <https://bitbucket.org/pypa/>`_ [2]_
* Distribute merged back into :ref:`setuptools`, and :ref:`setuptools` development
  migrated to the PyPA BitBucket account. [1]_ [5]_
* PyPI started supporting clients using verified SSL with standard cert bundles.
* PyPI forced web users over to SSL.
* :ref:`pip` (v1.3) and :ref:`easy_install <setuptools>` (v0.7) use
  verified SSL by default (`pip release notes`_)
* easy_install supports additional hashes beyond md5 (pip already did)
* `Fastly CDN enabled`_ for PyPI (donated)
* Restructured the `pip install docs
  <https://pip.pypa.io/en/latest/installing/>`_ to clarify that
  setuptools and pip are the "base" of the bootstrapping hierarchy
* setuptools available as a cross platform wheel on PyPI
* :pep:`438` and the associated pip changes.
* :ref:`pip` (v1.4) added support for building and installing :term:`wheels <pypug:Wheel>`
  (`pip release notes`_)
* :term:`pypug:Python Packaging Authority (PyPA)` became the maintainer for the
  `Python Packaging User Guide`_, which was forked from the "Hitchhiker's Guide
  to Packaging".
* Packaging Dev and User Summits were held at Pycon 2013 to share ideas on the
  future of packaging. [3]_ [4]_
* :pep:`425` and :pep:`427` were accepted.  Together,
  they specify a built-package format for Python called :term:`wheels <pypug:Wheel>`.

Before 2013
-----------

**2012-06-19**: The effort to include "Distutils2/Packaging" in Python 3.3 was
abandoned due lack of involvement. [6]_

**2011-02-28**: The :term:`pypug:Python Packaging Authority (PyPA)` is created
to take over the maintenance of :ref:`pip` and :ref:`virtualenv` from Ian Bicking,
led by Carl Meyer, Brian Rosner and Jannis Leidel. Other proposed names were
"ianb-ng", "cabal", "pack" and "Ministry of Installation".

**2008**: `distribute`_ was forked from :ref:`setuptools` by Tarek Ziade, in an
effort to create a more open project.

**2008**: :ref:`pip` was introduced by Ian Bicking as an alternative to
``easy_install`` (the installer included with :ref:`setuptools`)

**2007**: :ref:`virtualenv` was introduced by Ian Bicking, which allowed users
to create isolated Python environments based on a central system installation of
Python.

**2006**: :ref:`buildout` was introduced by Jim Fulton, with the goal to create
a system for repeatable installations of potentially complex projects.

**2005**: Package files could be hosted on PyPI for the first time,
`following the sprints at PyCon US 2005
<https://mail.python.org/pipermail/catalog-sig/2005-March/000518.html>`_.

**2004**: :ref:`setuptools` was introduced by Phillip Eby, which included the
`Egg <pypug:Egg>` format, and the ability to declare and automatically install
dependencies.

**2003**: :term:`PyPI <pypug:Python Package Index (PyPI)>` was up and running.

**2002**: Richard Jones started work on :term:`PyPI
<pypug:Python Package Index (PyPI)>`, and created :pep:`301` to describe it.

**2001**: :pep:`241` was written to standardize the metadata for distributions.

**2000**: `catalog-sig`_ was created to discuss creating a centralized index of
distributions.

**2000**: :ref:`distutils` was added to the Python standard library in Python 1.6.

**1998**: The `distutils-sig`_ dicussion list was created to discuss the
development of :ref:`distutils`.


.. _distutils-sig: https://www.python.org/community/sigs/current/distutils-sig/
.. _catalog-sig: https://www.python.org/community/sigs/retired/catalog-sig/
.. _`Python Packaging User Guide`: https://packaging.python.org
.. _peep: https://pypi.org/project/peep/
.. _`Fastly CDN enabled`: https://mail.python.org/pipermail/distutils-sig/2013-May/020848.html
.. _distribute: https://pypi.org/pypi/distribute
.. _`MOSS grant for PyPI`: https://pyfound.blogspot.com/2017/11/the-psf-awarded-moss-grant-pypi.html
.. _`OTF grant for PyPI awarded to PSF`: https://pyfound.blogspot.com/2019/03/commencing-security-accessibility-and.html
.. _`pip release notes`: https://pip.pypa.io/en/stable/news/
.. _`Old pypa-dev Google Group decommissioned`: https://groups.google.com/d/msg/pypa-dev/twf9HCGfv3k/t2HJwzF-AgAJ
.. _`Packaging Working Group used MOSS and CZI funding to improve pip dependency resolver`: https://pyfound.blogspot.com/2020/03/new-pip-resolver-to-roll-out-this-year.html
.. _`New pip dependency resolver released`: https://pyfound.blogspot.com/2020/11/pip-20-3-new-resolver.html
.. _`The PyPA became a PSF Fiscal Sponsoree`: https://www.python.org/psf/records/board/minutes/2021-01-27/#new-business


----

.. [1] https://mail.python.org/pipermail/distutils-sig/2013-June/021160.html
.. [2] https://mail.python.org/pipermail/distutils-sig/2013-March/020224.html
.. [3] https://us.pycon.org/2013/community/openspaces/packaginganddistributionminisummit/
.. [4] http://pyvideo.org/video/1731/panel-directions-for-packaging/
.. [5] https://mail.python.org/pipermail/distutils-sig/2013-March/020127.html
.. [6] https://mail.python.org/pipermail/python-dev/2012-June/120430.html
