.. _`PyPA Specifications`:

===================
PyPA Specifications
===================

In addition to maintaining the default implementation of the Python packaging
toolchain, the Python Packaging Authority is also responsible for maintaining
the interoperability specifications used to define the interactions between
those tools.

Active Specifications
---------------------

The currently active specifications are recorded in the
:ref:`PyPA Specifications <pypug:specifications>` section of the
Python Packaging User Guide.


Specification Update Process
----------------------------

PyPA interoperability specifications are separated into two categories:

* `Package Distribution Metadata <https://packaging.python.org/specifications/#package-distribution-metadata>`_
* `Package Index Interfaces <https://packaging.python.org/specifications/#package-index-interfaces>`_

For Package Distribution Metadata, the default responsible decision maker is
the lead CPython representative on distutils-sig.

For Package Index Interfaces, the default responsible decision maker is
the lead maintainer for the `Python Package Index <https://pypi.org>`__.

The current lead PyPI maintainer is Donald Stufft, while the current lead
CPython representative on distutils-sig is Nick Coghlan.


Handling fixes and other minor updates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Backwards compatible fixes and small enhancements to the specifications are
handled by submitting pull requests to the specifications section of the guide.
All enhancements proposed this way *must* be discussed

PyPA core reviewers are responsible for deciding which of these changes can
just be accepted (e.g. fixing a typo), which need to be reviewed by the relevant
responsible decision maker before being accepted, and which need to be escalated
to the full Python Enhancement Proposal process.


Handling new specifications and major updates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Proposals for new interoperability specifications or major changes to existing
ones should be formulated and submitted as Standards Track Python Enhancement
Proposals in accordance with :pep:`1`.

Such proposals must reference a PR against the PyPA Specifications section in
the Python Packaging User Guide that adds the new specification as a separate
file and updates the index of active specifications accordingly.

The ``Discussions-To`` header in packaging related PEPs should be set to
``distutils-sig@python.org``.

Whenever a new PEP is put forward on distutils-sig, any PyPA core
reviewer that believes they are suitably experienced to make the final
decision on that PEP may offer to serve as the BDFL's delegate (or
"PEP czar") for that PEP. If their self-nomination is accepted by the
other PyPA core reviewers, the lead PyPI maintainer and the lead
CPython representative on distutils-sig, then they will have the
authority to approve (or reject) that PEP.

Otherwise, the default BDFL-Delegate depends on the area the PEP affects:

* Package Distribution Metadata: lead CPython representative on distutils-sig
* Package Index Interfaces: lead PyPI maintainer

Proposals that require backwards incompatible changes to existing
interoperability specifications (and hence a new major version of the
specification rather than in-place updates) are currently not permitted. If
that policy is changed in the future, then some additional work will be needed
to define stable URLs that reference the active version of affected
specifications.


Handling existing specifications maintained as Informational PEPs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Historically, new interoperability specifications or major changes to existing
ones were handled as Informational Python Enhancement Proposals in accordance
with :pep:`1`. This proved problematic, as it meant the proposals were a mix
of both the specification itself, as well as the rationale for the
specification, which could make them difficult to read for tool implementors.
It also meant that new revisions needed to either leave the original version
active (requiring tool implementors to read both to get a clear view of what
they needed to implement) or else duplicate the original content (making it
harder to review just the changes to the specification).

For these existing specifications, the maintenance process is as follows:

* Fixes and other minor updates are handled as issues on the Python Packaging
  User Guide, and PRs to the `official PEPs repo <https://github.com/python/peps>`_
* If a major update is needed, then a Standards Track PEP should be written
  that includes migrating the affected specification fully to the Python
  Packaging User Guide based maintenance process as part of the proposal
