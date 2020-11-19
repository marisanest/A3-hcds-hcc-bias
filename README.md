# A3-hcds-hcc-bias

The goal of this project is to explore the concept of bias through data on Wikipedia articles. The project focuses on articles on political figures from a variety of countries. The analysis performed shows the coverage of politicians on Wikipedia and the quality of articles about politicians between countries.

## Data sources

As data source one API and two existing datasets are used.

#### 1. The ORES API ([documentation][1], [endpoint][2])

The ORES API is a service that provides information about the quality of revisions of Wikipedia articles.

#### 2. A dataset of **Wikipedia articles** ([documentation][3], [download][4])

This dataset contains data on most English-language Wikipedia articles within the category "Category:Politicians by nationality". It was published by by [Os Keyes][7] and licensed under the [CC-BY 4.0][8].

#### 3. A dataset of **country populations** ([documentation][5], [download][6]). 

This dataset includes information about the population of countries at the end of the year 2019. **Note**: the downloaded file was edited before. The resulting file can be found here: `src/_data/export_2019.csv`.

#### Licensing

For the ORES API and the country population dataset no licensing was found. So please make sure you are useing this data sources properly. All resulting datasets follow the same licensing policy as the Wikipedia articles dataset ([CC-BY 4.0][8]).

## Results

As result, you can find six `CSV`-formatted data files in the folder `results`. The six files show: 

#### 1. `country_coverage_data_top_10.csv`: The countries with the greatest coverage of politicians on Wikipedia compared to their population

| name | description |
|--------------|--------------|
| country | Country name |
| coverage | Coverage |

#### 2. `country_coverage_data_bottom_10.csv`: The countries with the least coverage of politicians on Wikipedia compared to their population

| name | description |
|--------------|--------------|
| country | Country name |
| coverage | Coverage |

#### 3. `country_relative_quality_data_top_10.csv`: The countries with the highest proportion of high quality articles about politicians

| name | description |
|--------------|--------------|
| country | Country name |
| relative_quality | Percentage of high quality articles of all articles |

#### 4. `country_relative_quality_data_bottom_10.csv`: The countries with the lowest proportion of high quality articles about politicians

| name | description |
|--------------|--------------|
| country | Country name |
| relative_quality | Percentage of high quality articles of all articles |

#### 5. `region_coverage_data.csv`: The ranking of geographic regions by coverage of politicians

| name | description |
|--------------|--------------|
| region | Region name |
| coverage | Coverage |

#### 6. `region_relative_quality_data.csv`: The ranking of geographic regions by proportion of high quality articles

| name | description |
|--------------|--------------|
| region | Region name |
| relative_quality | Percentage of high quality articles of all articles |

## Getting started

### Prerequisites

In order to use this project (espaccilay the jupyter note book), please ensure that you have a Python version greater or equal to `3.6.1`, a working installation of [Poetry][8] and [git][9] installed.

### Setup

1. Clone this repository (or use SSH) and move it into the repo root.

    git clone https://github.com/marisanest/A2-hcds-hcc.git
    cd A2-hcds-hcc

1. Install the dependencies in the repo root.

    poetry install

1. Create a subshell within the virtual environment by running:

    poetry shell

1. Open the project with Jupyter in your browser.

    jupyter notebook
    
----

[1]:https://ores.wikimedia.org/
[2]:https://ores.wikimedia.org/v3/
[3]:https://figshare.com/articles/Untitled_Item/5513449
[4]:https://ndownloader.figshare.com/files/9614893
[5]:https://www.prb.org/international/indicator/population/table/
[6]:https://datacenter.prb.org/download/international/indicator/population/csv
[7]:https://figshare.com/authors/Os_Keyes/660514
[8]:https://creativecommons.org/licenses/by/4.0/
