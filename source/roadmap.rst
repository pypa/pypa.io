.. _`PyPA Roadmap`:

============
PyPA Roadmap
============

:Last Reviewed: 2015-11-02

A status page for the  major PyPA Todo items that will determine the course of Python Packaging.


Core Standards
--------------

.. _`Metadata 2.0`:

Metadata 2.0
~~~~~~~~~~~~

:Summary: The next major upgrade of the metadata format, currently specified in
          `PEP426`_. The current version, 1.2, is specified in `PEP345`_.
          `PEP426`_ currently has a very broad scope, and will likely be
          trimmed, with the minimum scope being at least to include
          "build_requires" and "test_requires", and possibly the extensions
          system.

:PEP Src: `pep-0426-core-metadata.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0426-core-metadata.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP426
                 <https://github.com/pypa/interoperability-peps/labels/PEP426>`_

:Status: `PEP426`_ is in Draft status.


.. _`Environment Markers Update`:

Environment Markers Update
~~~~~~~~~~~~~~~~~~~~~~~~~~

:Summary: An update to the notion of "Environment Markers" introduced in
          `PEP345`_. `PEP426`_ was originally scoped to include this update, but
          it's being moved out to `PEP496`_.

:PEP Src: `pep-0496-environment-markers.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0496-environment-markers.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP496
                 <https://github.com/pypa/interoperability-peps/labels/PEP496>`_

:Status: `PEP496`_ is in Draft status.


.. _`Optional Dependencies ("Extras")`:

Optional Dependencies ("Extras")
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:Summary: An attempt to formalize the notion of "Extras" introduced by
          setuptools. `PEP426`_ was originally scoped to include this, but it
          will likely be broken out.

:Issues/PRs: `pypa/interoperability-peps/labels/Extras
                 <https://github.com/pypa/interoperability-peps/labels/Extras>`_

:Status: Currently covered in `PEP426`_ (which is in Draft status), but will
         likely be broken out.


.. _`Metadata Extensions`:

Metadata Extensions
~~~~~~~~~~~~~~~~~~~

:Summary: A system that supports extending metadata with custom
          metadata. `PEP426`_ was originally scoped to include this.  It's
          unclear, if it will remain, or be broken out.

:Issues/PRs: `pypa/interoperability-peps/labels/Extensions
                 <https://github.com/pypa/interoperability-peps/labels/Extensions>`_

:Status: Currently covered in `PEP426`_ (which is in Draft status), but may be
         broken out.


.. _`Standard Python Extensions`:

Standard Python Extensions
~~~~~~~~~~~~~~~~~~~~~~~~~~

:Summary: Assuming we support an extensions system, then this describes a set of
          standard extensions for Python packages.  This is currently specified
          in `PEP459`_ .

:PEP Src: `pep-0459-standard-metadata-extensions.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0459-standard-metadata-extensions.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP459
                 <https://github.com/pypa/interoperability-peps/labels/PEP459>`_

:Status: `PEP459`_ is in Draft status.


.. _`Build Neutrality`:

Build Neutrality
~~~~~~~~~~~~~~~~

:Summary: An attempt to specify a tool-neutral Build API, that pip will adopt,
          with the goal being to easily support other build systems besides
          setuptools/distutils.

:Issues/PRs: `pypa/interoperability-peps/labels/Build-Neutrality
                 <https://github.com/pypa/interoperability-peps/labels/Build-Neutrality>`_

:Status: Discussions are ongoing on distutils-sig.  Some proposals involve
         solutions that solve sdist 2.0 and build neutrality with a single plan.
         There is also some debate whether to initially support neutrality using
         ``setup.py`` as the interface, or to use something completely new.


.. _`sdist 2.0`:

Source Distribution 2.0
~~~~~~~~~~~~~~~~~~~~~~~

:Summary: A specification for a new sdist format.  The current setuptools sdist
          format has no formal specification.  It's up for debate whether this
          new format will be numbered "1.0" or "2.0".

:Issues/PRs: `pypa/interoperability-peps/labels/sdist-2.0
                 <https://github.com/pypa/interoperability-peps/labels/sdist-2.0>`_

:Status: Discussions are ongoing on distutils-sig.  Some proposals involve
         solutions that solve sdist 2.0 and build neutrality with a single plan.
         A central part of the discussion is whether sdists should (or can) be
         required to hold static metadata (vs. requiring a build command to
         generate the metadata).


.. _`Installation Database Updates`:

Installation Database Updates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:Summary: An update to the "dist-info" installation database format introduced
          in `PEP376`_.

:Issues/PRs: `pypa/interoperability-peps/labels/Installation-Database
                 <https://github.com/pypa/interoperability-peps/labels/Installation-Database>`_

:Status:  No current activity.


.. _`Wheel Updates`:

Wheel Updates
~~~~~~~~~~~~~

:Summary: An update to the wheel spec (`PEP427`_) largely to handle a tagging
          scheme for linux binary wheels, although there are various other
          issues that people have raised.

:Issues/PRs: `pypa/interoperability-peps/labels/Wheel
                 <https://github.com/pypa/interoperability-peps/labels/Wheel>`_

:Status:  No current activity.


.. _`Common Filename Scheme`:

Common Filename Scheme
~~~~~~~~~~~~~~~~~~~~~~

:Summary: This would be a replacement for `PEP425`_ that increases scope to also
          cover the naming scheme used for dist-info directories, installation
          DB metadata directories, sdist archives and wheel archives.

:Issues/PRs: `pypa/interoperability-peps/issues/48
                 <https://github.com/pypa/interoperability-peps/issues/48>`_

:Status: No current activity.


Tools & Systems
---------------

.. _`pip Dependency Resolution`:

pip Dependency Resolution
~~~~~~~~~~~~~~~~~~~~~~~~~

:Summary: pip currently has an overly-simplistic "first found, wins" resolver
          that ignores constraints already present in the environment.

:Issues/PRs: `pip/issues/988 <https://github.com/pypa/pip/issues/988>`_

:Status: Robert Collins is known to be working on a new resolver in
         `pip/pull/2716 <https://github.com/pypa/pip/pull/2716>`_

.. _`pip upgrade`:

pip upgrade [--all]
~~~~~~~~~~~~~~~~~~~

:Summary: Many pip users want a non-recursive upgrade (``pip upgrade -U`` is
          currently recursive), and many users also want some sort of ``pip
          upgrade --all`` command.

:Issues/PRs:  `pip/issues/59 <https://github.com/pypa/pip/issues/59>`_

:Status: Ongoing discussion in `pip/issues/59
         <https://github.com/pypa/pip/issues/59>`_.  A non-recursive
         implementation of ``pip upgrade`` exists in `pip/pull/3194
         <https://github.com/pypa/pip/pull/3194>`_


.. _`vendor distutils`:

Vendor distutils into setuptools
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:Summary: Possibly "vendor" a copy of distutils into setuptools, so that
          setuptools is free to evolve independent of the Standard Library copy
          of distutils.

:Issues/PRs: `setuptools/issues/417/adopt-distutils
        <https://bitbucket.org/pypa/setuptools/issues/417/adopt-distutils>`_

:Status: Under consideration.


.. _`Warehouse`:

The New & Improved PyPI
~~~~~~~~~~~~~~~~~~~~~~~

:Summary: A rehaul of PyPI built on `Warehouse <https://github.com/pypa/warehouse>`_

:Issues: `pypa/warehouse/issues <https://github.com/pypa/warehouse/issues>`_

:Status:  Under Development



.. _`TUF`:

PyPI Integrate TUF
~~~~~~~~~~~~~~~~~~

:Summary: An effort to integrate PyPI with the `"The Update Framework" (TUF)
          <http://www.updateframework.com/projects/project>`_.  This is
          specified in `PEP458`_

:PEP Src: `pep-0458-tuf-online-keys.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0458-tuf-online-keys.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP458
                 <https://github.com/pypa/interoperability-peps/labels/PEP458>`_

:Status:  `PEP458`_ is in Draft status.


Documentation
-------------

.. _`New PyPUG Tutorials`:

New PyPUG Tutorials
~~~~~~~~~~~~~~~~~~~

:Summary: An attempt to improve the 2 primary PyPUG tutorials for readability
          and style, to coincide with the launch of the new Warehouse-backed
          PyPI.

:Issues/PRs: `warehouse/issues/729 <https://github.com/pypa/warehouse/issues/729>`_

:Status: Nicole (from Warehouse team) and Marcus are working together on this
         along with a team of volunteer writers.


.. _`Specs vs PEPs`:

Specs vs PEPs
~~~~~~~~~~~~~

:Summary: An attempt to present finalized PEPs as non-numbered "Specifications"
          that are organized together in the PyPUG.  As it is, it's too hard to
          know what really represents the finalized set of PyPA PEPs.

:Issues/PRs: `pypa.io/issues/11 <https://github.com/pypa/pypa.io/issues/11>`_

:Status: Nick Coghlan has started working on migrating to this approach, using
         ``pypa.io/specifications/`` as the stable base URL.


.. _`PyPA PEP Process`:

PyPA PEP Process
~~~~~~~~~~~~~~~~

:Summary: At it's core, PyPA is consistent with the Python PEP process, but
          around the edges, it has a unique workflow that should be documented,
          with the goal being to increase involvement.  This process may change
          if the Python PEP database migrates to using gitlab as specified in
          `PEP507`_.

:Issues/PRs: `interoperability-peps/issues/53
        <https://github.com/pypa/interoperability-peps/issues/53>`_


:Status:  This is being worked on in conjunction with the :ref:`Specs vs PEPs`
          work.



.. _PEP345: http://www.python.org/dev/peps/pep-0345/
.. _PEP425: http://www.python.org/dev/peps/pep-0425/
.. _PEP426: http://www.python.org/dev/peps/pep-0426/
.. _PEP427: http://www.python.org/dev/peps/pep-0427/
.. _PEP376: http://www.python.org/dev/peps/pep-0376/
.. _PEP458: http://www.python.org/dev/peps/pep-0458/
.. _PEP459: http://www.python.org/dev/peps/pep-0459/
.. _PEP496: http://www.python.org/dev/peps/pep-0496/
.. _PEP507: http://www.python.org/dev/peps/pep-0507/
