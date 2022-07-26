# team-repo-template

***!!! For research purposes only !!!***

- [Template](#team-repo-template)
    - [Data](#data)
    - [Usage](#usage)
        - [Installation](#installation)
        - [Requirements](#requirements)
        - [Activate conda environment](#activate-conda-environment)
        - [Steps to run ](#steps-to-run)
            - [Step-1](#step-1)
            - [Step-2](#step-2)
    - [Contact information](#contact-information)

**Aim:** We aim to develop a pipeline for our project.

## Data

Input for this project is a .bam file.

## Usage

### Installation

Installation simply requires fetching the source code. Following are required:

- Git

To fetch source code, change in to directory of your choice and run:

```sh
git clone -b main \
    git@github.com:u-brite/team-repo-template.git
```

### Requirements

*OS:*

Currently works only in Linux OS. Docker versions may need to be explored later to make it useable in Mac (and
potentially Windows).

*Tools:*

- Anaconda3
    - Tested with version: 2020.02

### Activate conda environment

Change in to root directory and run the commands below:

```sh
# create conda environment. Needed only the first time.
conda env create --file configs/environment.yaml

# if you need to update existing environment
conda env update --file configs/environment.yaml

# activate conda environment
conda activate testing
```

### Steps to run


#### Step-1

```sh
python src/data_prep.py -i path/to/file.tsv -O path/to/output_directory
```

#### Step-2

```sh
python src/model.py -i path/to/parsed_file.tsv -O path/to/output_directory
```

Output from this step includes -

```directory
output_directory/
├── parsed_file.tsv               <--- used for model
├── plot.pdf- Plot to visualize data
└── columns.csv - columns before and after filtering step

```

**Note**: The is an example note with a [link](https://github.com/u-brite/team-repo-template).


## Contact information

For issues, please send an email with clear description to

Tarun Mamidi    -   tmamidi@uab.edu
Shaurita Hutchins - shutchins@uab.edu
