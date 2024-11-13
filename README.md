# Just_Superhuman

Just_Superhuman is an open-source genetic annotation module based on Prof. George Church's Protective and Enhancing Alleles spreadsheet ([link](https://arep.med.harvard.edu/gmc/protect.html)). The module is designed to produce genetic reports within the [Just-DNA-Seq platform](https://dna-seq.github.io/) and integrates with the OakVar genomic analysis framework.

## Overview

The module annotates user genomes to identify variants associated with beneficial phenotypes. It leverages multiple annotators to provide comprehensive insights:

- **dbSNP**
- **ClinVar**
- **OMIM**
- **NCBI Gene**
- **PubMed**
- **gnomAD**


## Installation

### Installation through OakVar

From the OakVar store, you can install the module through user interface or command line using:

```bash
ov module install just_superhuman
```

Alternatively, clone the repository directly into the "postaggregators" folder of OakVar:

```bash
git clone https://github.com/dna-seq/just_superhuman
```

### Manual Installation

1. Create a folder named `just_superhuman` in the `postaggregators` directory of OakVar.
2. Download or clone this repository into the `just_superhuman` folder.

## Usage

After installation, the module can be used within the OakVar framework to generate detailed genetic reports from your VCF files. It can be integrated into existing pipelines or used independently to annotate variants of interest.

## Challenges and Development Notes

While developing the module, we encountered challenges due to incomplete data in the original spreadsheet, such as missing rsIDs, coordinates, and allele information. We manually supplemented these details and, in some cases, evaluated all existing variants within certain genes to identify the most relevant ones. We also included variants likely to cause desired effects based on homologous genes from other species.

Applying the module to real genomes highlighted the need for stricter variant selection criteria. Many identified variants did not correlate with the expected phenotypes. We are actively refining the module to improve its accuracy and are exploring additional data sources like gene expression data and protein-protein interaction networks to enhance annotations.

## Example Report

An example report generated using this module is available [here](https://github.com/dna-seq/just_superhuman/blob/main/example/antonkulaga.vcf.superhuman.html). This report illustrates the annotations and potential insights the module can provide.

## Future Work

We aim to:

- **Improve Accuracy**: Refine variant selection criteria to reduce false positives.
- **Enhance Data Integration**: Incorporate additional data sources for more comprehensive annotations.
- **Validation**: Collaborate with researchers to validate the module on genomes of individuals exhibiting the relevant phenotypes.

## Contributing

We welcome contributions from the community to enhance the module's functionality and accuracy. Feel free to submit issues or pull requests on our [GitHub repository](https://github.com/dna-seq/just_superhuman).

---

**Note**: This module is under development. While it provides valuable insights, it should be used for research purposes and not as a resource for clinical decision-making.