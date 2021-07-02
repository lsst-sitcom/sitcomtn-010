.. image:: https://img.shields.io/badge/sitcomtn--010-lsst.io-brightgreen.svg
   :target: https://sitcomtn-010.lsst.io
.. image:: https://github.com/lsst-sitcom/sitcomtn-010/workflows/CI/badge.svg
   :target: https://github.com/lsst-sitcom/sitcomtn-010/actions/

####################################################################################
Announcement of Opportunity: Community Engagement with Rubin Observatory Commissioning Effort
####################################################################################

SITCOMTN-010
============

The Vera C. Rubin Observatory invites members of the US and Chilean LSST science communities to join the Project Commissioning Team in order to make value-added contributions that facilitate an efficient transition into LSST Operations. In this Announcement of Opportunity (AO) we include descriptions of its purpose, examples of value-added contributions, terms and conditions for participation, and the process to respond to this AO via submitted Letters of Interest (LOIs).

The anticipated total value-added contribution via this program is of order 15-20 FTE of effort. This effort will likely be distributed across a larger number of individuals and preferably organized into discrete groups of like interests and skills, and performed over a roughly two-year period that includes calendar years 2022 and 2023. Financial support associated with this AO is limited, and non-Rubin-staff members of the Commissioning Team are generally expected to have other sources of support (limited travel and local accommodation support to enable on-site work at key activity centers in Tucson, SLAC, and Chile can be made available).

Links
=====

- Live drafts: https://sitcomtn-010.lsst.io
- GitHub: https://github.com/lsst-sitcom/sitcomtn-010

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-sitcom/sitcomtn-010

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the ``acronyms.tex`` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
