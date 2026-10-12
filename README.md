# Sequential Addition Kinetic Elucidation (SAKE): Experimental Data, Processing and Kinetic Analysis

## Project Overview

Sequential Addition Kinetic Elucidation (SAKE) is a one-pot experimental protocol for obtaining multiple kinetic datasets through sequential reagent additions within a single reaction vessel. By generating different concentration regimes during a single experiment, SAKE reduces the number of independent experiments required for kinetic investigations while minimising experiment-to-experiment variability.

The method was demonstrated using nucleophilic aromatic substitution (SNAr) reactions between aryl phenyl ethers and secondary amines, involving competing uncatalysed and amine-base-catalysed reaction pathways. Combined with Automatic Variable Time Normalisation Analysis (Auto-VTNA) and microkinetic modelling, SAKE enables the determination of reaction orders, rate constants, and other kinetic parameters.

This repository provides the experimental datasets, Python code for data processing and kinetic analysis, and supporting resources for reproducing and extending the work.

**Associated publication:** Dalland, D., Atkins, A. P., Schrecker, L. and Hii, K. K. M., *‘One-pot’ kinetic profiling of SNAr reactions via Sequential Addition Kinetic Elucidation (SAKE)*, Reaction Chemistry & Engineering (2026). [https://doi.org/10.1039/D6RE00214E](https://doi.org/10.1039/D6RE00214E)
Please find the previous studies that this work builds upon in the references list. 

## Experimental SAKE Protocol

SAKE experiments were performed using sequential additions of reagents, with reaction progress monitored using in situ infrared (IR) spectroscopy and high-performance liquid chromatography (HPLC).

The experimental setup, reagent addition protocol, alternative experiment designs, HPLC sampling procedures, and experiment catalogue are described in detail in Section 2 of the publication's [Supporting Information](https://pubs.rsc.org/re/article/doi/10.1039/d6re00214e/1297993/One-pot-kinetic-profiling-of-SNAr-reactions-via#supplementary-data).

## Experimental Data Processing

The repository includes Python code and Excel files documenting the preparation of kinetic datasets from the experimental measurements.

The data-processing workflow is organised into the following folders:

- **[HPLC calibration](https://github.com/ddalland/SAKE/tree/main/HPLC%20calibration):** Calibration data and supporting files used for quantitative HPLC analysis.
- **[Processing HPLC data](https://github.com/ddalland/SAKE/tree/main/Processing%20HPLC%20data):** Code and representative examples for processing of peak-area-vs time csv data from the Agilent Chemstation software.
- **[Excel files with HPLC analysis](https://github.com/ddalland/SAKE/tree/main/Excel%20files%20with%20HPLC%20analysis):** Excel files used for converting HPLC peak area ratio data into time-versus-concentration datasets using the calculated concentrations of internal standard for each period of the SAKE experiment.  in  including corrections for changes in reaction mixture volume during sequential additions.
- **[Scaling and visualising IR data](https://github.com/ddalland/SAKE/tree/main/Scaling%20and%20visualising%20IR%20data):** Processing and visualisation of in situ IR data.
- **[Scaling of IR trends with calibrated HPLC data](https://github.com/ddalland/SAKE/tree/main/Scaling%20of%20IR%20trends%20with%20calibrated%20HPLC%20data):** Code and input data for scaling of IR concentration profiles using calibrated HPLC measurements and SAKE addition information to obtain kinetic datasets.

Further methodological details are provided in Section 3 of the [Supporting Information](https://pubs.rsc.org/re/article/doi/10.1039/d6re00214e/1297993/One-pot-kinetic-profiling-of-SNAr-reactions-via#supplementary-data).

## Kinetic Datasets and Modelling

The kinetic analysis combines Auto-VTNA for reaction-order determination with microkinetic modelling based on ordinary differential equations (ODEs). Details of the kinetic models, fitting procedures, and model comparisons are provided in Section 4 of the Supporting Information.
The processed kinetic datasets, dataset analysis codes and rate-constant analysis files (Eyring, Bronsted and Hammett) are organised into the following folders:

- **[SAKE datasets](https://github.com/ddalland/SAKE/tree/main/SAKE%20datasets):** Processed kinetic datasets from the SAKE experiments.
- **[SAKE dataset analysis](https://github.com/ddalland/SAKE/tree/main/SAKE%20dataset%20analysis):** Python code and supporting files for kinetic analysis of the SAKE datasets, organised into two subfolders:
  - **Auto-VTNA:** Analysis of concentration–time datasets to determine reaction orders through optimisation of time-normalised reaction progress overlays.
  - **ODE modelling:** Microkinetic modelling using ordinary differential equations (ODEs) to evaluate proposed kinetic models, fit rate constants, and compare simulated concentration profiles with experimental data.
- **[Eyring Hammett and Bronsted Analyis](https://github.com/ddalland/SAKE/tree/main/Eyring%20Hammett%20and%20Bronsted%20Analyis):** Supporting analysis of temperature, substituent, and amine effects.
- **[Solvent effect study](https://github.com/ddalland/SAKE/tree/main/Solvent%20effect%20study):** Datasets and supporting files for the investigation of solvent effects.

## Kinetic Analysis Using Auto-VTNA

Auto-VTNA is a freely available Python-based tool for automatic kinetic analysis, allowing reaction orders to be determined by optimising the overlay of time-normalised concentration profiles.

Auto-VTNA was used extensively in the SAKE study. For more information, see the [Auto-VTNA GitHub repository](https://github.com/ddalland/Auto-VTNA), which includes the Python source code, Jupyter notebook tutorials, and links to YouTube tutorials demonstrating the graphical user interface (GUI).

The latest version of the Auto-VTNA GUI can be downloaded [here](https://drive.google.com/file/d/1ra1YQUa2ypbiGOw_JDwpM1DaLxHaxTH5/view).

For questions about the SAKE protocol, data processing, or kinetic analysis, please contact me through GitHub.
