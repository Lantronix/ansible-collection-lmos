=========================================
Lantronix LMOS Collection Release Notes
=========================================

.. contents:: Topics

v1.0.4
======

Minor Changes
-------------

- ``.ansible-lint`` -- adopted the Red Hat certified-collection configuration
  (``profile: production``, ``no-log-password`` in ``warn_list``); the lint
  scope now covers ``playbooks/`` and sanity ignore files.
- ``iqoq_validate.yml`` -- uses fully qualified collection names throughout
  and a generic example hostname in the usage comment.
- ``tests/config.yml`` -- declares ``python_requires`` (Python 3.9+).
- Removed sanity ignore entries that are not permitted for certified
  collections; the ``import`` sanity test now passes with ``ansible.netcommon``
  installed.
- CI: added sanity, lint, and Red Hat certification-checker workflows with
  Dependabot tracking for GitHub Actions.

v1.0.3
======

Minor Changes
-------------

- ``README.md`` -- removed the stale self-referential archive banner left over
  from the migration off the personal fork.
- ``README.md`` -- removed the "Build and install from source tarball" install
  path; Automation Hub and GitHub clone cover supported customer installs.
- ``README.md`` -- removed the ``Testing`` section (unit tests, sanity tests,
  live device tests); this is contributor/CI documentation, not customer-facing.

v1.0.2
======

Minor Changes
-------------

- ``README.md`` -- added ``Changelog`` section linking to ``CHANGELOG.rst``
  per Red Hat Automation Hub certification feedback.
- ``README.md`` -- replaced relative ``LICENSE`` link with absolute URL so
  the link resolves correctly when rendered on Automation Hub.

v1.0.1
======

Bugfixes
--------

- ``meta/runtime.yml`` -- bumped ``requires_ansible`` from ``>=2.15.0`` to ``>=2.16.0``
  to meet Red Hat Automation Hub certification requirement (AAP 2.4 lifecycle).
- ``galaxy.yml`` -- updated repository, documentation, and issues URLs to the official
  Lantronix GitHub organization (``github.com/Lantronix``).

v1.0.0
======

New Plugins
-----------

- ``lantronix.lmos.lmos`` terminal plugin -- handles LMOS ANSI escape sequences and prompt detection via SSH
- ``lantronix.lmos.lmos`` cliconf plugin -- provides CLI command interface for LMOS devices

New Modules
-----------

- ``lantronix.lmos.lmos_facts`` -- gather structured facts from an LMOS device (version, model, serial, hostname, management IP)
