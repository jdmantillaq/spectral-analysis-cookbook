# Spectral Analysis for Geophysical Data Cookbook

<img src="thumbnails/spectral_analysis.png" alt="thumbnail" width="300"/>

[![nightly-build](https://github.com/ProjectPythia/spectral-analysis-cookbook/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/spectral-analysis-cookbook/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/spectral-analysis-cookbook/main?labpath=notebooks)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21139295.svg)](https://doi.org/10.5281/zenodo.21139294)


This Project Pythia Cookbook covers **spectral analysis methods for geophysical data in Python**, with a focus on Fourier and harmonic analysis, spectral filtering, and Empirical Orthogonal Function (EOF) analysis. The notebooks build foundational skills for analyzing climate time series and gridded datasets, then apply these techniques to real atmospheric observations. Applications include frequency decomposition, **Extended EOF (EEOF)** analysis, and r**egression of atmospheric fields onto diagnostic indices**.

## Motivation

Many important climate signals, from the seasonal cycle to the interannual and long term variability, are best understood in **frequency space**. This cookbook teaches you how to move from raw geophysical time series to meaningful diagnostics: removing the annual cycle with harmonic regression, designing and applying spectral filters, interpreting power spectra and extracting dominant patterns with EOF/PCA.

By the end, you will be able to preprocess climate data for variability studies, decompose fields by frequency band, and carry out EOF analyses on datasets—including **time-extended EOFs** and **multivariable EOFs**.

## Authors

Juan Diego Mantilla, Sreedevi Puthiyamadam Vasu, Robert R. Ford, Suyue Li, Alex Blackmer, Yiqun Tian, Arman Oliazadeh

### Contributors

<a href="https://github.com/ProjectPythia/spectral-analysis-cookbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/spectral-analysis-cookbook" />
</a>

## Structure

### Data Analysis Methods

Foundational notebooks cover core spectral and decomposition tools:

- **Harmonic analysis** of seasonal cycles in time series.
- **Harmonic regression** to remove annual-cycle harmonics from atmospheric fields.
- **Fourier analysis** for decomposition, dominant timescales, and spectral filtering.
- **The Gibbs phenomenon** and spectral leakage at discontinuities.
- **2D/3D - EOF/PCA**, including temporal vs. spatial formulations.

### Data Analysis Applications

Applied workflows on real atmospheric and oceanic datasets:

- **Seasonal-cycle removal compared**: daily climatology vs. harmonic regression on 850-hPa zonal wind, with spectral checks for residual annual power.
- **Zonal-wind frequency decomposition**: FFT partitioning of interannual, annual, semiannual, and intraseasonal variability.
- **Extended EOF (EEOF) analysis** of tropical OLR to capture propagating modes missed by standard EOF pairs.
- **Spectral analysis of tropical variability and the MJO**: Welch spectra, red-noise significance, 20–90-day bandpass filtering, and Hovmöller diagnostics on OLR and zonal wind.
- **Multivariate EOFs** of OLR and zonal wind to extract a coupled MJO signal and build an RMM-like index.
- **Regression onto climate indices and PCs**, including RMM-based MJO circulation and convection patterns.
- **Machine learning**: Comparison of neural networks trained using raw anomalies versus filtered intraseasonal (~20-90 days) anomalies to forecast 850-hPa zonal wind at subseasonal (~14 days) lead times for a specific location (Nairobi, Kenya). Future plans include developing additional ML models for temperature and precipitation and comparing predictive skill with RMM-based models.

## Running the Notebooks

You can either run the notebooks in the Cookbook using [Binder](https://binder.projectpythia.org/) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org/), which enables "one click"
execution in the cloud. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon (see screenshots [here](https://foundations.projectpythia.org/preamble/how-to-use/#running-pythia-foundations-examples)),
and a text box will appear. Type or paste the Pythia Binder link
(`https://binder.projectpythia.org`) and click "Launch".
After a few moments you should be presented with a
notebook that you can interact with. You’ll be able to execute code
and even change the example programs. At first the code cells
have no output, until you execute them by pressing
{kbd}`Shift`{kbd}`Enter`. Complete details on how to interact with
a live Jupyter notebook are described in the Pythia Foundations chapter [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter).

Note, not all Cookbook chapters are executable. If you do not see
the rocket ship icon, such as on this page, you are not viewing an
executable book chapter.

### Running on Your Own Machine

If you are interested in running this material locally on your computer, you will need to follow this workflow:

(Replace "cookbook-example" with the title of your cookbooks)

1. Clone the `https://github.com/ProjectPythia/spectral-analysis-coobook` repository:
  ```bash
    git clone https://github.com/ProjectPythia/spectral-analysis-coobook.git
  ```
2. Move into the `spectral-analysis-coobook` directory
  ```bash
   cd spectral-analysis-coobook
  ```
3. Create and activate your conda environment from the `environment.yml` file
  ```bash
   conda env create -f environment.yml
   conda activate spectral-cookbook-dev
  ```
4. Move into the `notebooks` directory and start up Jupyterlab
  ```bash
   cd notebooks/
   jupyter lab
  ```

