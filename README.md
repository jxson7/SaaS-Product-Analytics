 [![CC BY 4.0][cc-by-shield]][cc-by] [![DOI](https://zenodo.org/badge/doi/10.5281/zenodo.16106711.svg)](https://doi.org/10.5281/zenodo.16106711)

 # SaaS Product Analytics

 This repository contains my exploratory analysis of Software-as-a-Service (SaaS) pricing models over time.  
 **Owner / maintainer:** GitHub user `jxson7`.

 The analysis focuses on correlating subscription states, feature sets, and pricing across multiple years for a curated set of SaaS products.

## Origin of the data and sources

This project is **inspired by and builds on** the laboratory package available at [`isa-group/SaaS-analysis`](https://github.com/isa-group/SaaS-analysis).

The structure of the dataset, the choice of SaaS products, and some of the analytical ideas are inspired by the laboratory package accompanying the paper:

 > *"iSubscription: Bridging the Gap Between Contracts and Runtime Access Control in SaaS" (ICSOC 2025)*  
 > DOI: [10.5281/zenodo.16106711](https://doi.org/10.5281/zenodo.16106711)

 Where I reuse or adapt data or ideas from that package, they remain subject to the original **CC BY 4.0** license, with full attribution to the original authors. This repository adds my own analysis, code, and figures on top of those ideas.

 ## Studied SaaS and coverage

 The following SaaS products and years are in scope for the analysis. The symbols indicate the status of each SaaS for the indicated year:

 - ✅: The SaaS is modeled for the indicated year.  
 - ✖️: There is a snapshot, but a clear feature list cannot be extracted.  
 - ❌: There isn't a snapshot for the SaaS in the indicated year.

 | SaaS          | 2019 | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 |
 | ------------- | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
 | Box           |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Buffer        |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Canva         |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | CircleCI      |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | ClickUp       |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Clockify      |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Crowdcast     |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Databox       |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Deskera       |  ❌  |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Dropbox       |  ✖️  |  ✖️  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Evernote      |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Figma         |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | GitHub        |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Hypercontext  |  ❌  |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ❌  |
 | Jira          |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | MailChimp     |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Microsoft 365 |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Notion        |  ✖️  |  ✖️  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Okta          |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | OpenPhone     |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Overleaf      |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Planable      |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Postman       |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Pumble        |  ❌  |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Quip          |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Salesforce    |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Shopify       |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Slack         |  ✅  |  ✅  |  ❌  |  ❌  |  ✅  |  ✅  |  ✅  |
 | Tableau       |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Trello        |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Trustmary     |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | UserGuiding   |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Webflow       |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Wrike         |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Zenhub        |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Zoom          |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |  ✅  |
 | Zapier        |  ✅  |  ✅  |  ❌  |  ✅  |  ✅  |  ✅  |  ✅  |

 **TOTAL:** 240 pricings – 37 SaaS.

 ## Repository structure (this project)

 This repository currently contains:

 - `data/`: Data files used by the notebook (e.g., SaaS pricing snapshots and derived datasets).  
 - `figures/`: Figures generated from the analysis.  
 - `main.ipynb`: Jupyter notebook that performs the analysis and produces figures.  
 - `requirements.txt`: Python dependencies needed to run the notebook.

 As the project evolves, additional notebooks, scripts, or configuration files may be added.

 ## Usage

 ### Install dependencies

 You can install the Python dependencies with:

 ```bash
 pip install -r requirements.txt
 ```

 Then open `main.ipynb` in Jupyter, VS Code, or another compatible environment and execute the cells.

 ## Licensing and attribution

 Unless otherwise noted, my own code and documentation in this repository are provided under the same **CC BY 4.0** terms to remain compatible with the original lab package.

 When using this repository or derived results, please:

 - Cite the original paper and Zenodo package:  
   *"iSubscription: Bridging the Gap Between Contracts and Runtime Access Control in SaaS"*, DOI [10.5281/zenodo.16106711](https://doi.org/10.5281/zenodo.16106711).
 - Optionally reference this repository (GitHub user `jxson7`) if you build on the analyses provided here.

 [cc-by]: https://creativecommons.org/licenses/by/4.0/
 [cc-by-shield]: https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg

