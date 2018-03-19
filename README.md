# Metagenomic Workflow Collaboration (mwc)

[![Snakemake](https://img.shields.io/badge/snakemake-≥3.12.0-brightgreen.svg)](https://snakemake.bitbucket.io)
[![Build Status](https://travis-ci.org/snakemake-workflows/mwc.svg?branch=master)](https://travis-ci.org/snakemake-workflows/mwc)

This repo contains the code for a Snakemake workflow of the Metagenomic
Workflow Collaboration (mwc). The current focus is a barebones metagenomics
analysis workflow to produce primary output files from several different
metagenomic analysis tools. 

## Authors

* Fredrik Boulund (@boulund)
* Lisa Olsson (@lis4matilda)
* (your name here)

## Usage

### Step 1: Install workflow
<!--download and extract the [latest release](https://github.com/snakemake-workflows/mwc/releases). -->

If you simply want to use this workflow, clone the repository: `git clone
git@github.com:boulund/mwc`.  If you intend to modify and further develop this
workflow, fork this reposity. Please consider providing any generally
applicable modifications via a pull request.

If you use this workflow in a paper, don't forget to give credits to the
authors by citing the URL of this repository and, if available, its DOI (see
above).

### Step 2: Configure workflow

Configure the workflow according to your needs via editing the file
`config.yaml`.

### Step 3: Execute workflow

Test your configuration by performing a dry-run via

    snakemake -n

Execute the workflow locally via

    snakemake --cores $N

using `$N` cores or run it in a cluster environment via

    snakemake --cluster qsub --jobs 100

or

    snakemake --drmaa --jobs 100

See the [Snakemake documentation](https://snakemake.readthedocs.io) for further
details.

## Testing

The ambition is that mwc will contain extensive tests to verify functionality.
Test cases are in the subfolder `tests`. They should be executed via continuous
integration with Travis CI. 


## Contributing

1. Fork or clone the repository.
2. Create a branch with a descriptive name based on your intended changes using
   dashes to separate words, e.g. `branch-to-add-megahit-assembly-step`
3. Insert your code into the respective folders, i.e. `scripts`, `rules` and
   `envs`. Define the entry point of the workflow in the `Snakefile` and the
   main configuration in the `config.yaml` file.
4. Commit changes to your local fork/clone.
5. Create a pull request (PR) with some motivation behind the work you have
   done and possibly some explanations for tricky bits. 

