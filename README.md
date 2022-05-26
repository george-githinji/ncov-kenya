# Kenya-specific SARS-CoV-2 Nextstrain analysis

## Get the workflow
```bash 
https://github.com/george-githinji/ncov-KE
```

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
