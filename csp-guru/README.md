# CSP.guru
An open-source database of all concentrating solar power plants of the world for energy modellers and analysts. This version of CSP.guru reflects the status of CSP projects as of 1 July 2020.

## About
This dataset holds technical, economic, financial, and industrial data on all operating concentrating solar power stations and of stations under construction, as well as several pilot stations. For detailed description of the data collection procedure, please see the initial article for which the dataset was compiled [Lilliestam et al. (2017)](https://doi.org/10.1038/nenergy.2017.94).


## Data Package
We provide the data in form of a [tabular data package](https://frictionlessdata.io/specs/tabular-data-package/) that consists of a CSV (comma separated values) file holding the actual data and a single JSON file (`datapackage.json`) holding the metadata.


## License and conditions
The licence of this data allows to share and adapt this data if you give appropriate credit, under the [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/) license.
For academic and professional use (presentations, journal articles, reports, etc): Please cite the original source, the paper [Lilliestam et al. (2020)](https://doi.org/10.1080/15567249.2020.1773580). Please also link to www.csp.guru if possible.

## Changes in this version of CSP.guru
This is the second version of CSP.guru produced during the openCSP project. The Noor Energy 1 project and Dubai and Cerro Dominador in Chile were updated to reflect recent developments. Both projects were checked for the role of colocated PV on their economics, and expected generation was deleted to reflect the fact that CSP-only generation is unknown. The GPS locations were converted to decimal for better handling. Additional data on the Chinese CSP stations was included based on information from [Chuncheng Zang](mailto:zangchch@mail.iee.ac.cn) and [Alina Gilmanova](mailto:alina@mail.iee.ac.cn).

### New Columns
The versions of CSP.guru produced in the openCSP project beginning with [2020-01-01] contain 50 additional columns compared to the prior csp.guru [2019-01-01] version. We added a lot of technical information from the NREL/Solarpaces database. The LCOE and other economics calculations has been made more transparent by adding columns on intermediary results including specific cost and currency deflation.


### Changes in projects
The number of projects was increased compared to csp.guru[2019-01-01] version, because we included all research and pilot stations previously contained in the NREL/Solarpaces database.


## Contact
For questions or issues get in touch with [Johan Lilliestam](mailto:johan.lilliestam@iass-potsdam.de) or [Richard Thonig](mailto:richard.thonig@iass-potsdam.de).


## Acknowledgements
Funding for this version [2020-07-01] and the previous version [2020-01-01] came from SolarPACES in the  openCSP data project.
Funding for previous versions: the [2016-08-30 version](https://doi.org/10.5281/zenodo.1342716)  of csp.guru was supported by a European Research Council Consolidator Grant [DESERTECTION (grant number 313553)](https://cordis.europa.eu/project/rcn/106709_de.html),the [2018-05-14 version of csp.guru](https://doi.org/10.5281/zenodo.1318152) and [2019-01-01 version of csp.guru](https://doi.org/10.5281/zenodo.3466625) received support from the European Union Horizon 2020 research and innovation program [MUSTEC (grant agreement No 764626) ](https://cordis.europa.eu/project/rcn/211264_en.html).
