================
The Work of PyPA
================


The :ref:`distutils` cross-platform build and distribution system was added to
the Python standard library in late 2000. This means the current Python software
distribution ecosystem (which builds on :ref:`distutils`) has a foundation that
is almost 15 years old, which poses a variety of challenges to successful
evolution.

The current effort to improve the situation started when the ``packaging``
library (also known as ``distutils2``) `did not make it
<https://mail.python.org/pipermail/python-dev/2012-June/120430.html>`_ into the
standard library for Python 3.3.  That effort had spanned from 2009 to 2012.

The current effort is managed by the :term:`Python Packaging Authority (PyPA)`,
in cooperation with members of the Python core development team.


Goals
=====

* To provide a relatively easy to use software distribution infrastructure that
  is also fast, reliable and reasonably secure.  "Reasonably secure", due to
  backwards compatibility constraints preventing turning off some insecure
  legacy features.

* Although it's still being defined, to work towards a "Meta-Packaging" [1]_ system that:

  * Clearly delineates the phases of distribution
  * Allows for multiple interacting tools vs one monolithic tool
  * Specifically allows for alternative build systems, i.e. a `"MetaBuild"
    <http://www.python.org/dev/peps/pep-0426/#metabuild-system>`_ system.

* To improve the docs for users, including the `Python Packaging User Guide`_,
  anything related to packaging on `docs.python.org`_, and the project docs for
  :ref:`pip`, :ref:`setuptools`, :ref:`virtualenv`, and :ref:`wheel`.

* To be progressive, but also be very mindful to not break things that are
  currently working, due to haste.

* To specifically *not* focus at first on adding something to the standard
  library as our solution to our packaging problems.  Adding something to the
  standard library is hard, and once it's added, it's a slow process to change
  it.  Most of the current effort is largely focused on 3rd party projects.

.. _docs.python.org: http://docs.python.org


How to help
===========

* Get involved with one of mainstream :ref:`packaging projects
  <pypug:projects>`.
* Help us catalog and discuss the current problems in packaging and
  installation.  See the `The issue tracker for the problems in packaging
  <https://github.com/pypa/packaging-problems/issues>`_ maintained by
  :term:`PyPA <Python Packaging Authority (PyPA)>`.
* Submit Issues and PRs to the `PyPA PEP Development Repository
  <https://github.com/pypa/interoperability-peps>`_
* Discuss pretty much anything related to packaging at `distutils-sig
  <http://mail.python.org/mailman/listinfo/distutils-sig>`_.


Presentations & Articles
========================

In addition to this document, there have been some talks and presentations
regarding current and future efforts related to packaging.

* PyCon US, March 2013

  * `Directions in Packaging Q & A Panel (aka "./setup.py install must die")
    <http://pyvideo.org/video/1731/panel-directions-for-packaging>`__

* PyCon AU, July 2013

  * `Nobody Expects the Python Packaging Authority
    <http://pyvideo.org/video/2197/nobody-expects-the-python-packaging-authority>`__

* linux.conf.au 2014

  * Python Packaging 2.0: Playing Well With Others (`video
    <https://www.youtube.com/watch?v=7An2GobbSWU>`_, `article
    <http://lwn.net/Articles/580399>`_)

* PyCon US, April 2014

  * `What is coming in Python packaging
    <https://us.pycon.org/2014/schedule/presentation/204/>`_
  * `Python packaging simplified, for end users, app developers, and open source
    contributors <https://us.pycon.org/2014/schedule/presentation/219>`_

* Personal essays

  * `Nick Coghlan
    <http://python-notes.curiousefficiency.org/en/latest/pep_ideas/core_packaging_api.html>`__


----

.. [1] See Nick Coghlan's `The Phases of Distribution
       <http://python-notes.curiousefficiency.org/en/latest/pep_ideas/core_packaging_api.html#the-phases-of-distribution>`_
       and `A Meta-Packaging System
       <http://python-notes.curiousefficiency.org/en/latest/pep_ideas/core_packaging_api.html#a-meta-packaging-system>`_

.. _Python Packaging User Guide: http://packaging.python.org
