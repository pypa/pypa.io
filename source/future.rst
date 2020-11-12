==========
PyPA Goals
==========


The :ref:`distutils` cross-platform build and distribution system was added to
the Python standard library in late 2000. This means the current Python software
distribution ecosystem (which builds on :ref:`distutils`) has a foundation that
is almost 15 years old, which poses a variety of challenges to successful
evolution.

The current effort to improve the situation started when the ``packaging``
library (also known as ``distutils2``) `did not make it
<https://mail.python.org/pipermail/python-dev/2012-June/120430.html>`_ into the
standard library for Python 3.3.  That effort had spanned from 2009 to 2012.

The current effort is managed by the :term:`pypug:Python Packaging Authority (PyPA)`, in cooperation with members of the
Python core development team.

PyPA's current goals are:

* To provide a relatively easy to use software distribution infrastructure that
  is also fast, reliable and reasonably secure.  "Reasonably secure", due to
  backwards compatibility constraints preventing turning off some insecure
  legacy features.

* Although it's still being defined, to work towards a "Meta-Packaging" [1]_ system that:

  * Clearly delineates the phases of distribution
  * Allows for multiple interacting tools vs one monolithic tool
  * Specifically allows for alternative build systems, i.e. a `"MetaBuild"
    <https://www.python.org/dev/peps/pep-0518/>`_ system.

* To improve the docs for users, including the `Python Packaging User Guide`_,
  anything related to packaging on `docs.python.org`_, and the project docs for
  :ref:`pip`, :ref:`setuptools`, :ref:`virtualenv`, and :ref:`wheel`.

* To be progressive, but also be very mindful to not break things that are
  currently working, due to haste.

* To specifically *not* focus at first on adding something to the standard
  library as our solution to our packaging problems.  Adding something to the
  standard library is hard, and once it's added, it's a slow process to change
  it.  Most of the current effort is largely focused on 3rd party projects.

.. _docs.python.org: https://docs.python.org


----

.. [1] See Nick Coghlan's `The Phases of Distribution
       <http://python-notes.curiousefficiency.org/en/latest/pep_ideas/core_packaging_api.html#the-phases-of-distribution>`_
       and `A Meta-Packaging System
       <http://python-notes.curiousefficiency.org/en/latest/pep_ideas/core_packaging_api.html#a-meta-packaging-system>`_

.. _Python Packaging User Guide: https://packaging.python.org
