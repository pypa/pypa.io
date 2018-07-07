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

Interoperability specifications maintained by the Python Packaging Authority
are tracked as Informational Python Enhancement Proposals in accordance
with :pep:`1`.

The currently active specifications are recorded in the
:ref:`PyPA Specifications <pypug:specifications>` section of the
Python Packaging User Guide.

This section may also include clarifications, amendments and additional
guidance for specification implementors in cases where the corresponding
PEPs have yet to be updated appropriately.


Specification Update Process
----------------------------

PyPA interoperability specifications are separated into two categories:

* `Package Distribution Metadata <https://packaging.python.org/specifications/#package-distribution-metadata>`_
* `Package Index Interfaces <https://packaging.python.org/specifications/#package-index-interfaces>`_


Proposing new specifications
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Proposals for new interoperability specifications should be formulated and
submitted as new Informational Python Enhancement Proposals in accordance
with :pep:`1`.

Such proposals must be accompanied by a PR against the PyPA Specifications
section in the Python Packaging User Guide that adds a new subsection defining
the purpose of the new specification and the role it plays in the wider Python
packaging ecosystem.

The ``Discussions-To`` header in packaging related PEPs should be set to
``distutils-sig@python.org``.

Whenever a new PEP is put forward on distutils-sig, any PyPA core
reviewer that believes they are suitably experienced to make the final
decision on that PEP may offer to serve as the BDFL's delegate (or
"PEP czar") for that PEP. If their self-nomination is accepted by the
other PyPA core reviewers, the lead PyPI maintainer and the default
BDFL delegate for package distribution metadata PEPs, then they will have the
authority to approve (or reject) that PEP.

Otherwise, the default BDFL-Delegate depends on the area the PEP affects.

* Package Distribution Metadata PEPs: Paul Moore
* Package Index Interface PEPs: Donald Stufft

For Package Distribution Metadata, the default BDFL-Delegate was
originally appointed directly by Guido van Rossum as Python's BDFL (hence the
use of the term ``BDFL-Delegate``), but is now nominated by the previous
default BDFL-Delegate (and the transfer of delegation approved by Guido).

For Package Index Interfaces, the default responsible decision maker is
the lead maintainer for the `Python Package Index <https://pypi.org>`__.

Provisional Acceptance
~~~~~~~~~~~~~~~~~~~~~~

PyPA has its own variant of the standard library's provisional modules, which
is provisional interoperability specifications.

These are specifications which have been accepted for implementation in the
core packaging tools (PyPI, pip, etc), but are still considered subject to
potentially backwards incompatible amendments if real world experience
indicates that there are critical problems in the interface design that make
it hard to implement and/or use correctly.

When a PEP has only been provisionally accepted, this will be noted in the
text of the affected PEP.

Handling fixes and other minor updates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The preferred approach to handling corrections and clarifications for all
recent interoperability specifications is to designate in the PEP that
the actively maintained version of the specification is hosted in the
:ref:`PyPA Specifications <pypug:specifications>` section of the user guide,
and the PEP process is used solely to propose and review changes to the
specifications, rather than serving as long term interface documentation in
their own right.

For an example of this approach, see :pep:`566`.

This allows readability improvements that don't affect software interoperability
to be implemented using the Python Packaging User Guide's standard pull request
based workflow, in a process that more closely matches the relationship between
the :ref:`Python language reference <https://docs.python.org/dev/reference/>`
and the Python Enhancement Proposals that update it.

If a change being considered this way has the potential to affect software
interoperability, then it must be escalated to the distutils-sig mailing list
for discussion, where it will be either approved as a text-only change, or
else directed to the PEP process for specification updates.

For older PEPs, where the PEP itself serves as the reference documentation,
the equivalent amendment process is to submit an issue and/or pull
request against the `official PEPs repo <https://github.com/python/peps>`_.

All enhancements proposed this way *must* be discussed on distutils-sig prior
to amending the PEP, and any changes made after PEP acceptance must be
explicitly documented in a "Changes" section in the PEP itself. For example,
see:

* `Changes in PEP 440 <https://www.python.org/dev/peps/pep-0440/#summary-of-changes-to-pep-440>`_
* `Changes in PEP 503 <https://www.python.org/dev/peps/pep-0503/#changes>`_

PyPA core reviewers that are also PEP editors are responsible for deciding which
of these changes can just be accepted (e.g. fixing a typo), which need to be
reviewed by the relevant responsible decision maker before being accepted, and
which need to be escalated to the full Python Enhancement Proposal process.


Handling major updates
~~~~~~~~~~~~~~~~~~~~~~

For package distribution metadata, proposals that require backwards
incompatible changes to existing interoperability specifications for
package distribution metadata (and hence a new major version of the
specification rather than an in-place update) are currently not permitted.

This policy has been introduced based on historical experience that such
incompatibilities lead to the community sticking with older versions of the
metadata format indefinitely rather than upgrading to the revised format.

For package index interfaces, major updates are handled as either Process or
Standards Track PEPs targeting the Python Package Index as the reference
implementation. All such PEPs that introduce backwards incompatible changes
are required to define a suitable transition plan for affected software
publishers and tool developers.
