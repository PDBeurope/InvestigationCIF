# InvestigationCIF

## Overview

The [MMCIF investigation dictionary](dist/mmcif_investigation_fraghub_ext.dic) provides the data 
representation to capture relationships between macromolecule structures deposited in the wwPDB, 
and data from other database, with enrichment of additional information / metadata to describe 
an investigation -- aka a series of related structures that were collected for a project and 
together provide insight. 

This dictionary is an extension of the [PDBx/mmCIF](http://mmcif.wwpdb.org) dictionary
and provides the additional defintions required to handle require to generate the investigation 
files. Investigation files are umbrella files for a set of coordinate and their corresponding 
experimental data files. The example here is for data generated as part of a fragment-screening 
investigation where a number of atomic-level models are determined.

The mmCIF Investigation dictionary currently has over X new data categories and Y new data items.

## Organization of the repository

[README.md](README.md) - this file

[MMCIF investigation extension](dist/mmcif_investigation_fraghub_ext.dic) - Investigation dictionary extension

[MMCIF investigation](dist/mmcif_investigation_fraghub.dic) - Investigation dictionary extension merged with the parent PDBx/mmCIF dictionary

[examples](examples) - directory with examples of investigation mmCIF file(s) compliant with the MMCIF investgation dictionary
