# CSP.guru
A database of concentrating solar power plants of the world for energy modellers and analysts.
## About
This dataset holds technical, economic, financial, and industrial data on all operating concentrating solar power stations and of stations under construction (larger than 10 MW). For detailed description of the data collection procedure, please see the original article [Lilliestam et al. (2017)](https://doi.org/10.1038/nenergy.2017.94).
## Data Package
We provide the data in form of a [tabular data package](https://frictionlessdata.io/specs/tabular-data-package/) that consists of a CSV (comma separated values) file holding the actual data and a single JSON file (`datapackage.json`) holding the metadata.
## License and conditions
The licence of this data allows academic and all non-commercial use if you give appropriate credit, under the [Creative Commons Attribution-NonCommercial 4.0 International license](https://creativecommons.org/licenses/by-nc/4.0/).
For academic and professional use (presentations, journal articles, reports, etc):
Please cite the original source, the paper [Lilliestam et al. (2017)](https://doi.org/10.1038/nenergy.2017.94). Please also link to www.csp.guru if possible.
## Changes in this version of CSP.guru
The data collection for this version of CSP guru has been conducted by Johan Lilliestam and Richard Thonig in the first half of 2020. It is based on the [May 2019 Version]( https://doi.org/10.5281/zenodo.1342716 ) by Johan Lilliestam, Mercè Labordena and Lana Ollier. The data reflects the situation of CSP projects and industry on January first of 2019. For this iteration of the dataset we decided to limit it to materializing projects, i.e. those under construction and those already commissioned. Moreover, we added the status of decommissioned plant, as both SEGS I and II have reached the end of their lifetime. Additionally, the following changes in the structure of the data were implemented compared to the last version.
### New Columns
We added the columns Support_currency and Cost_currency to indicate the currency, i.e. EURO, RMB, USD, etc. of both Support and Total_cost. For the companies along the supply chain: i.e. Developer,	EPC,	HCE,	SCA we added a column with the respective home countries of the companies to enable the analysis of the localisation of the industry. We reconceptualized the SCA column to the company engineering the SCA or Heliostat, and not the actual manufacturing, which is often subcontracted to local companies.
### Changes in projects
In terms of projects we decided to limit the dataset to stations that are either under construction or have been commissioned. We exclude stations that are under development or have an unclear status. Therefore, we have excluded projects that are part of the NER 300 program, projects that we found no progress information on, and also excluded projects that were awarded at some point but have not broken ground.  The following projects could not be confirmed to be under construction, as far as we know:
* Alba Nova 1
* Abhijeet
* Aurora
* Kogan Creek
* Diwakar
* KVK Energy Solar Project
* MINOS
* Noor Midelt
* Redstone
* Stillwater

The Chinese stations  do not have specific names but are often referred to by the company building them, the region or city as well as the technology used in the project. Consequently, we updated the naming schema to include as much of this information as possible, still we could not find progress information on the following projects and have therefore excluded them from the update:

* CECIC Gansu Wuwei - 100MW Trough
* Dahua Shangyi - 50MW Tower
* Golden Tower / Gansu Jinta / China Three Gorges New Energy Jinta - 100MW Tower
* Golmud - 2 x 100MW Tower
* Huaneng Urat Fresnel (Northern United Power Urat) - 50MW Fresnel
* Huanghe Delingha - 135MW Tower
* Shenzen Jinfan Akesai - 50MW Trough
* Shouhang  Yumen (Old name: Shenhua Guohua Yumen) - 100MW Tower,
* Zhangjiakou Terasolar (Huaqiang Zhaoyang Zhangjiakou DSG 50 CLFR) - 50MW Fresnel
* Zhengbei (CITIC Zhenbei) - 50MW Fresnel
* Zhongyang Zhangjiakou Chabei - 64MW Trough

### Financial information
The financial information was reduced compared to the last version. We have not produced LCOE and remuneration for other currencies than the USD and have updated the base year for the LCOE calculation to 2018.

## Contact
For questions or issues get in touch with [Johan Lilliestam](mailto:johan.lilliestam@usys.ethz.ch) or [Richard Thonig](mailto:richard.thonig@usys.ethz.ch).
## Acknowledgements
Funding for the [2016-08-30 version](https://doi.org/10.5281/zenodo.1342716)  of this work came from a European Research Council Consolidator Grant [DESERTECTION (grant number 313553)](https://cordis.europa.eu/project/rcn/106709_de.html),the [2018-05-14 version](https://doi.org/10.5281/zenodo.1318152) received support from the European Union Horizon 2020 research and innovation program [MUSTEC (grant agreement No 764626) ](https://cordis.europa.eu/project/rcn/211264_en.html).
