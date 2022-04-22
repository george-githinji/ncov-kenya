# Kenya-specific SARS-CoV-2 Nextstrain analysis

## Get the workflow

Download the ncov workflow.

``` bash
git clone https://github.com/nextstrain/ncov.git
cd ncov/
```

This directory contains the logic to run a Nextstrain analysis for SARS-CoV-2 based on a workflow build configuration you provide.

## Get the workflow build configuration

Download the workflow build configuration into the `ncov/` workflow directory.

``` bash
git clone https://github.com/blab/ncov-kenya.git .
```

All configuration files for the Kenya workflow live in the resulting `ncov-kenya/` directory.

## Download data

Follow [instructions to curate data from GISAID search and downloads](https://docs.nextstrain.org/projects/ncov/en/latest/analysis/data-prep.html#curate-data-from-gisaid-search-and-downloads).
Specifically, search for "Africa / Kenya" in the search interface and download the "Africa" bundle from the "nextregions" downloads on GISAID.
Save the Kenya data to the `ncov/` directory in the `data/` subdirectory as `kenya.tar`.
Compress the Kenyan data with `gzip data/kenya.tar`.
Save the Africa nextregions file to the `ncov/data/` directory as `africa.tar.gz`.

## Run the workflow

Run the workflow with the Nextstrain CLI (or Snakemake, if you prefer), specifying the build configuration file in the `ncov-kenya/` directory.

``` bash
nextstrain build . --cores 4 -p --configfile ncov-kenya/builds_kenya.yaml
```

## View the analysis output

View the analysis output locally by running the Nextstrain CLI (or Auspice, if you prefer) and navigating to the corresponding server address in your browser.

``` bash
nextstrain view auspice/
```
