# InvestigationCIF
 ![Category count](https://badgen.net/static/Categories/17/orange) ![Item count](https://badgen.net/static/Items/122/purple) ![license](https://badgen.net/static/license/CC-0%201.0/gray) ![version](https://badgen.net/static/version/1.0.6.1/blue)

## Overview

This repository contains a [MMCIF investigation dictionary](dist/mmcif_investigation.dic) that provides a data representation to capture the relationships between macromolecule structures deposited in the worldwide Protein Data Bank (wwPDB), and data from other databases and databanks, with enrichment of additional information / metadata to describe an investigation -- aka a series of related structures that were collected for a project and together provide insight.

This dictionary is an extension of the [PDBx/mmCIF](http://mmcif.wwpdb.org) dictionary and provides the additional definitions required for an investigation files. Investigation files are umbrella files for a set of coordinates / models and their corresponding experimental data files. 

The primary example showcased here is for fragment screening investigations, where multiple atomic-level models are determined to analyze how small molecule fragments interact with protein targets, facilitating drug discovery efforts.

## Why InvestigationCIF?

Traditional PDB entries represent individual structures, but many research projects generate collections of related structures. InvestigationCIF solves this problem by:

- Creating umbrella files that link multiple coordinate files and their experimental data
- Adding contextual metadata about the overall investigation goals and methods
- Enabling better discoverability and analysis of related structural data
- Supporting reproducible research through standardized metadata capture


## Investigation Files

Fragment Screening Investigation mmCIF files created from PDB group depositions are available at:
https://ftp.ebi.ac.uk/pub/databases/msd/fragment_screening/investigations/

## Creating Investigation MMCIF file

An **investigation mmCIF file** can be created through [mmcif-gen](https://pypi.org/project/mmcif-gen/), which is a Python tool for generating mmCIF files.

mmcif-gen can be used to create an **investigation mmCIF file** from internal databases at research facilities, such as a synchrotron, for example:

```
# Fetch configuration for a specific facility
mmcif-gen fetch-facility-json maxiv

# Specify custom output directory
mmcif-gen fetch-facility-json maxiv -o ./mapping_operations
```

Each facility stores their data internally in different formats, thus each facility has a different facility-json.


For more extensive documentation on using it: 
<center>
 
[check mmcif-gen PyPI page](https://pypi.org/project/mmcif-gen/)
<br>
--or-- <br>
[check mmcif-gen GitHub repository](https://github.com/PDBeurope/Investigations)
</center>

## Organization of the repository

[README.md](README.md) - this file

[MMCIF investigation extension](dist/mmcif_investigation.dic) - Investigation dictionary extension

[Examples](examples) - directory with examples of investigation mmCIF file(s) compliant with the MMCIF investgation dictionary

## Contributions / collaborations

Fragment-based-screening (FBS) is a complex and data-rich endeavour, wherein each stage of the process can generate different file types of complex data, in both raw and processed forms. 
The popularity of fragment screening in academic scientific research and the pharmaceutical industry is reflected by the increasing number of facilities, such as synchrotrons, that support fragment screening experiments. 

Synchrotrons are central service centres that support experimental data generation with multiple options related to structural biology using X-ray crystallography. 

Individuals from synchrotrons across Europe were involve in developing the data model for fragment-screening in this repository. 
The [Protein Data Bank in Europe](https://www.ebi.ac.uk/pdbe/), in collaboration with [other organizations from the worldwide Protein Data Bank](https://www.wwpdb.org/), has led the project.

Synchrotrons and associated facilities involved in developing this data model:

* [The Crystallisation Facility](https://www.embl.org/services-facilities/grenoble/high-throughput-crystallisation/) at the [European Molecular Biology Laboratory (EMBL) Grenoble]( https://www.embl.org/research/faculty/grenoble/) and [European Synchrotron Radiation Facility (ESFR)]( https://www.esrf.fr/home.html/) in France
* [XChem: Diamond Fragment Screening](https://www.diamond.ac.uk/Instruments/Mx/Fragment-Screening.html) at [Diamond Light Source (DLS)](https://www.diamond.ac.uk/Home.html) in the United Kingdom
* [Fragment Screening Facility](https://www.helmholtz-berlin.de/forschung/oe/ps/macromolecular-crystallography/fragment-screening/index_en.html) at [Berlin synchrotron BESSY-MX and Helmholtz-Zentrum Berlin/HZB](https://www.helmholtz-berlin.de/forschung/quellen/bessy/index_en.html) in Germany
* [FragMAX](https://www.maxiv.lu.se/beamlines-accelerators/science-initiatives/fragmax-biomax-fragment-screening-platform/) at Swedish synchrotron [MAX IV](https://www.maxiv.lu.se/) in Sweden

<p></p>
  <a href="https://www.esrf.fr/home.html">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/ESRF_Logo.jpg?raw="true" alt="European Synchrotron Radiation Facility Logo" width="200">
  </a>
<br>
  <a href="https://www.embl.org/">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/EMBL_logo_colour_DIGITAL.png?raw="true" alt="European Molecular Biology Laboratory Logo" width="250">
  </a>
<br>
  <a href="https://www.diamond.ac.uk/Home.html">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/Diamond_Logo.jpg?raw="true" alt="Diamond Light Source Synchrotron Logo" width="250">
  </a>
<br>
  <a href="https://www.helmholtz-berlin.de/index_en.html">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/HZB_Logo.jpg?raw="true" alt="Helmholtz-Zentrum Berlin Research Center Logo" width="300">
  </a>
<br>
  <a href="https://www.maxiv.lu.se/">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/MAX%20IV_Logo.jpg?raw="true" alt="Max IV Synchrotron Logo" width="250">
  </a>
<br>
<br>
  <a href="https://www.ebi.ac.uk/pdbe/">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/PDBe_Logo.png?raw="true" alt="Protein Data Bank in Europe" width="250">
  </a>
<br>
<p></p>

## Funded by:

<p></p>
<span style="display: inline-block">
  <a href="https://inext-discovery.eu/">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/iNEXT_Discovery_Logo.png?raw="true" alt="iNext-Discovery Logo" width="200"></a>
</span>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<span style="display: inline-block;">
  <a href="https://fragmentscreen.org/home">
  <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/Fragment_Screen_Logo.png?raw="true" alt="FragmentScreen Logo" width="200"></a>
</span>
<p></p>

* [iNEXT-Discovery](https://inext-discovery.eu/) - a European Union funded project via Horizon Europe (Grant agreement ID: 871037)
* [FragmentScreen](https://fragmentscreen.org/home) - a European Union funded project via Horizon Europe (Grant agreement ID: 101094131)

<p></p>
 <img src="https://github.com/PDBeurope/InvestigationCIF/blob/main/logo/EN_FundedbytheEU_RGB_POS.png?raw="true" alt="Funded by the European Union" width="400">
<p></p>

<p></p>

## License

Available to all in accordance with the [Creative Commons Zero (CC0)](https://creativecommons.org/public-domain/cc0/) designation.

## Contributing

We welcome contributions to improve the InvestigationCIF dictionary. 
For changes, please open an issue first to discuss what you would like to change.

## Feedback

For any feedback or suggestions, email us at pdbehelp@ebi.ac.uk. Please include 'InvestigationCIF' in your subject line.
