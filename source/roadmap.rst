.. _`PyPA Roadmap`:

============
PyPA Roadmap
============

:Last Reviewed: 2020-07-20

A status page for the  major PyPA Todo items that will determine the course of Python Packaging.


Core Standards
--------------

.. _`Metadata 2.0`:

Metadata 2.0
~~~~~~~~~~~~

:Last Reviewed: 2020-06-08

:Summary: Major upgrades of the metadata format. Version 1.2 was specified in
	  :pep:`345`. :pep:`426` is `in Withdrawn status
          <https://www.python.org/dev/peps/pep-0426/#note-on-pep-history>`_; it
          had a very broad scope, and included "build_requires" and
	  "test_requires", and the extensions system.

:PEP Src: `pep-0426-core-metadata.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0426-core-metadata.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP426
                 <https://github.com/pypa/interoperability-peps/labels/PEP426>`_

:Status:
         :pep:`566` (Metadata 1.3) was accepted in February 2018. :pep:`566`
	 (Metadata 2.1) was accepted in February 2018. Several features of
	 Metadata 2.0 are specified but not yet accepted or implemented.


.. _`Environment Markers Update`:

Environment Markers Update
~~~~~~~~~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: An update to the notion of "Environment Markers" introduced in
          :pep:`345`. :pep:`426` was originally scoped to include this update, but
          it was moved out to :pep:`496`.

:PEP Src: `pep-0496-environment-markers.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0496-environment-markers.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP496
                 <https://github.com/pypa/interoperability-peps/labels/PEP496>`_

:Status: :pep:`496` has been rejected in favor of the more
         comprehensive :pep:`508`.


.. _`Optional Dependencies ("Extras")`:

Optional Dependencies ("Extras")
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: An attempt to formalize the notion of "Extras" introduced by 
          setuptools. :pep:`426` was originally scoped to include this, 
          but it will likely be broken out.

:Issues/PRs: `pypa/interoperability-peps/labels/Extras
                 <https://github.com/pypa/interoperability-peps/labels/Extras>`_

:Status: Currently covered in :pep:`426` (which is in Deferred status), but will
         likely be broken out.


.. _`Metadata Extensions`:

Metadata Extensions
~~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: A system that supports extending metadata with custom
          metadata. :pep:`426` was originally scoped to include this.  It's
          unclear, if it will remain, or be broken out.

:Issues/PRs: `pypa/interoperability-peps/labels/Extensions
                 <https://github.com/pypa/interoperability-peps/labels/Extensions>`_

:Status: Currently covered in :pep:`426` (which is in Deferred status), but may be
         broken out.


.. _`Standard Python Extensions`:

Standard Python Extensions
~~~~~~~~~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: Assuming we support an extensions system, then this describes a set of
          standard extensions for Python packages.  This is currently specified
          in :pep:`459`.

:PEP Src: `pep-0459-standard-metadata-extensions.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0459-standard-metadata-extensions.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP459
                 <https://github.com/pypa/interoperability-peps/labels/PEP459>`_

:Status: :pep:`459` is `in Deferred
         status <https://www.python.org/dev/peps/pep-0459/#pep-deferral>`_.


.. _`Build Neutrality`:

Build Neutrality
~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

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

:Last Reviewed: 2017-12-10

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

:Last Reviewed: 2017-12-10

:Summary: An update to the "dist-info" installation database format introduced
          in :pep:`376`.

:Issues/PRs: `pypa/interoperability-peps/labels/Installation-Database
                 <https://github.com/pypa/interoperability-peps/labels/Installation-Database>`_

:Status:  No current activity.


.. _`Wheel Updates`:

Wheel Updates
~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: An update to the wheel spec (:pep:`427`) largely to handle a tagging
          scheme for linux binary wheels, although there are various other
          issues that people have raised.

:Issues/PRs: `pypa/interoperability-peps/labels/Wheel
                 <https://github.com/pypa/interoperability-peps/labels/Wheel>`_

:Status:  No current activity.


.. _`Common Filename Scheme`:

Common Filename Scheme
~~~~~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: This would be a replacement for :pep:`425` that increases scope to also
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

:Last Reviewed: 2020-06-08

:Summary: pip currently has an overly-simplistic "first found, wins" resolver
          that ignores constraints already present in the environment.

:Issues/PRs: `pip/issues/988 <https://github.com/pypa/pip/issues/988>`_

:Status: The Packaging Working Group of the Python Software Foundation
	 `successfully applied for funding
	 <https://wiki.python.org/psf/PackagingWG#Dependency_resolver_and_user_experience_improvements_for_pip>`_
	 to finish the overhaul of the resolver, and a team is working
	 on the project. A pip release including the new resolver is
	 expected in 2020.

.. _`pip upgrade`:

pip upgrade [--all]
~~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

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

:Last Reviewed: 2017-12-10

:Summary: Possibly "vendor" a copy of distutils into setuptools, so that
          setuptools is free to evolve independent of the Standard Library copy
          of distutils.

:Issues/PRs: `setuptools/issues/417/adopt-distutils
        <https://bitbucket.org/pypa/setuptools/issues/417/adopt-distutils>`_

:Status: Under consideration.


.. _`TUF`:

PyPI Integrate TUF
~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2020-06-08

:Summary: An effort to integrate PyPI with the `"The Update Framework" (TUF)
          <https://theupdateframework.github.io>`_.  This is specified in :pep:`458`

:PEP Src: `pep-0458-tuf-online-keys.rst
          <https://github.com/pypa/interoperability-peps/blob/master/pep-0458-tuf-online-keys.rst>`_

:Issues/PRs: `pypa/interoperability-peps/labels/PEP458
                 <https://github.com/pypa/interoperability-peps/labels/PEP458>`_

:Status: :pep:`458` is in Accepted status. The PSF's Packaging Working
         Group received funding from Facebook and `a team is currently
         working on implementing TUF on PyPI
         <https://wiki.python.org/psf/PackagingWG#Warehouse:_Facebook_gift>`_.


Documentation and Governance
----------------------------

.. _`New PyPUG Tutorials`:

New PyPUG Tutorials
~~~~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: An attempt to improve the 2 primary PyPUG tutorials for readability
          and style, to coincide with the launch of the new Warehouse-backed
          PyPI.

:Issues/PRs: `warehouse/issues/729 <https://github.com/pypa/warehouse/issues/729>`_

:Status: Nicole (from Warehouse team) and Marcus are working together
         on this along with a team of volunteer writers; see
         `pypa/python-packaging-user-guide/tree/master/source/tutorials <https://github.com/pypa/python-packaging-user-guide/tree/master/source/tutorials>`_.


.. _`Specs vs PEPs`:

Specs vs PEPs
~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: An attempt to present finalized PEPs as non-numbered "Specifications"
          that are organized together in the PyPUG.  As it is, it's too hard to
          know what really represents the finalized set of PyPA PEPs.

:Issues/PRs: `pypa.io/issues/11 <https://github.com/pypa/pypa.io/issues/11>`_

:Status: Nick Coghlan has started working on migrating to this approach, using
         ``pypa.io/specifications/`` as the stable base URL.


.. _`PyPA PEP Process`:

PyPA PEP Process
~~~~~~~~~~~~~~~~

:Last Reviewed: 2017-12-10

:Summary: At its core, PyPA is consistent with the Python PEP process, but
          around the edges, it has a unique workflow that should be documented,
          with the goal being to increase involvement.  This process may change
          if the Python PEP database migrates to using GitLab as specified in
          :pep:`507`.

:Issues/PRs: `interoperability-peps/issues/53
        <https://github.com/pypa/interoperability-peps/issues/53>`_


:Status:  This is being worked on in conjunction with the :ref:`Specs vs PEPs`
          work.


.. _`PyPA Governance`:

PyPA Governance
~~~~~~~~~~~~~~~

:Last Reviewed: 2020-07-20

:Summary: :pep:`609` suggests a governing model that aims to formalize
	  existing practices.

:Status:
         :pep:`609` is approved. The PyPA and the Steering Council will
         continue to discuss and refine the scope of the PEP process,
         how and when it applies to packaging-specific standards and
         architecture decisions, and how we all might adapt governance
         processes further.
