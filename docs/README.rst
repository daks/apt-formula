.. _readme:

apt-formula
================

|img_travis| |docs| |img_sr|

.. |img_travis| image:: https://travis-ci.com/saltstack-formulas/apt-formula.svg?branch=master
   :alt: Travis CI Build Status
   :scale: 100%
   :target: https://travis-ci.com/saltstack-formulas/apt-formula
.. |docs| image:: https://readthedocs.org/projects/docs/badge/?version=latest
   :alt: Documentation Status
   :scale: 100%
   :target: https://apt-formula.readthedocs.io/en/latest/?badge=latest
.. |img_sr| image:: https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg
   :alt: Semantic Release
   :scale: 100%
   :target: https://github.com/semantic-release/semantic-release

A SaltStack formula that is empty. It has dummy content to help with a quick
start on a new formula and it serves as a style guide.

.. contents:: **Table of Contents**

General notes
-------------

See the full `SaltStack Formulas installation and usage instructions
<https://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html>`_.

If you are interested in writing or contributing to formulas, please pay attention to the `Writing Formula Section
<https://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html#writing-formulas>`_.

If you want to use this formula, please pay attention to the ``FORMULA`` file and/or ``git tag``,
which contains the currently released version. This formula is versioned according to `Semantic Versioning <http://semver.org/>`_.

See `Formula Versioning Section <https://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html#versioning>`_ for more details.

Contributing to this repo
-------------------------

**Commit message formatting is significant!!**

Please see :ref:`How to contribute <CONTRIBUTING>` for more details.

Available states
----------------

.. contents::
   :local:


``apt.dist_upgrade``
^^^^^^^^^^^^^^^^^^^^

Runs ``apt-get -y dist-upgrade``.

``apt.update``
^^^^^^^^^^^^^^

Runs ``apt-get -y update``.

``apt.upgrade``
^^^^^^^^^^^^^^^

Runs ``apt-get -y upgrade``.

``apt.repositories``
^^^^^^^^^^^^^^^^^^^^

Allows you to configure and manage repositories from pillar. Check ``pillar.example``
to see possible values. If used and no repositories are provided, sane default
values from ``map.jinja`` are used.

Check https://wiki.debian.org/SourcesList for an explanation about the resulting
files structure.

``apt.preferences``
^^^^^^^^^^^^^^^^^^^

Allows you to configure and manage apt's preferences from pillar. Check
``pillar.example`` to see possible values. If used and no repositories are
provided, sane default values from ``map.jinja`` are used.

Check https://wiki.debian.org/AptPreferences?action=show&redirect=preferences
and ``man 5 apt_preferences`` for an explanation about the resulting files structure.

``apt.ppa``
^^^^^^^^^^^
Installs ``python-software-properties``
(``$ /usr/bin/apt-add-repository ppa:user/repository``).

``apt.unattended``
^^^^^^^^^^^^^^^^^^
Installs and configures ``unattended-upgrades``

``apt.transports.debtorrent``
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Installs ``apt-transport-debtorrent``.

``apt.transports.https``
^^^^^^^^^^^^^^^^^^^^^^^^
Installs ``apt-transport-https``.

