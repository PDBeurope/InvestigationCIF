# InvestigationCIF
 ![Category count](https://badgen.net/static/Categories/22/orange) ![Item count](https://badgen.net/static/Items/192/purple) ![license](https://badgen.net/static/license/CC-0%201.0/gray) ![version](https://badgen.net/static/version/1.0.5/blue)
## Overview

The [MMCIF investigation dictionary](dist/mmcif_investigation_fraghub_ext.dic) provides the data representation to capture relationships between macromolecule structures deposited in the wwPDB, and data from other database, with enrichment of additional information / metadata to describe an investigation -- aka a series of related structures that were collected for a project and together provide insight. 

This dictionary is an extension of the [PDBx/mmCIF](http://mmcif.wwpdb.org) dictionary and provides the additional defintions required for an investigation files. Investigation files are umbrella files for a set of coordinate and their corresponding experimental data files. The primary example showcased here is for fragment screening investigations, where multiple atomic-level models are determined to analyze how small molecule fragments interact with protein targets, facilitating drug discovery efforts.

## Why InvestigationCIF?
Traditional PDB entries represent individual structures, but many research projects generate collections of related structures. InvestigationCIF solves this problem by:

- Creating umbrella files that link multiple coordinate files and their experimental data
- Adding contextual metadata about the overall investigation goals and methods
- Enabling better discoverability and analysis of related structural data
- Supporting reproducible research through standardized metadata capture


## Investigation Files
Fragment Screening Investigation files created from PDB group depositions are available at:
https://ftp.ebi.ac.uk/pub/databases/msd/fragment_screening/investigations/

## Creating Investigation MMCIF file
The Investigation mmcif can be created through [mmcif-gen]([https://pypi.org/project/mmcif-gen/](https://github.com/PDBeurope/Investigations), a Python tool for generating mmCIF files (using metadata from facilities):

```
# Fetch configuration for a specific facility
mmcif-gen fetch-facility-json dls-metadata

# Specify custom output directory
mmcif-gen fetch-facility-json dls-metadata -o ./mapping_operations
```
For more extensive documentation on using it: [ check here](https://pypi.org/project/mmcif-gen/).

## Organization of the repository

[README.md](README.md) - this file

[MMCIF investigation extension](dist/mmcif_investigation_fraghub_ext.dic) - Investigation dictionary extension

[Examples](examples) - directory with examples of investigation mmCIF file(s) compliant with the MMCIF investgation dictionary

## Contributing
We welcome contributions to improve the InvestigationCIF dictionary. For changes, please open an issue first to discuss what you would like to change.

## Feedback
For any feedback or suggestions, email us at pdbehelp@ebi.ac.uk. Please include 'InvestigationCIF' in your subject line.
