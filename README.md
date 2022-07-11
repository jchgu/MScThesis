# Overview

Millions of children worldwide are "left behind" at home communities as their parents migrate away for work. Parents' labor migration increases household income but decreases parental care, thereby exerting mixed influences on child development outcomes like educational attainment. To what extent do different arrangements of parental migration affect children's educational performance in the short term?

You can reproduce the results of my master's thesis using R with this replication package. 

# Data Availability and Provenance Statements

My thesis uses the data from [China Education Panel Survey (CEPS)](http://ceps.ruc.edu.cn/English/Home.htm), including both wave 1 and wave 2. The data is subject to a redistribution restriction, but it is freely available from [Chinese National Survey Data Archive](http://www.cnsda.org/index.php) (registration required). The website is only in Chinese; You can use Google translate to navigate.

Below are the links to CEPS datasets and documentations:

- [Wave 1 baseline](http://www.cnsda.org/index.php?r=projects/view&id=72810330)  To download datasets, click links #20 `Student Data` and #21 `Parent Data`. To download questionnaires, click links #13 `Student Questionnaire for Grade 7` and #12 `Parent Questionnaire for Grade 7`.

- [Wave 2 follow-up](http://www.cnsda.org/index.php?r=projects/view&id=61662993) To download datasets, click links #17 `学生问卷数据（英文）` and #18 `	家长问卷数据（英文）`. To download questionnaires, click links #6 `学生问卷(英文）` and #7 `家长问卷(英文）`.

## Statement about Rights

- [x] I certify that the author of the manuscript has legitimate access to and permission to use the data. 

## Summary of Availability

- [x] All data are publicly available.

## Dataset list

| Data files                                                   | Source | Notes               | Provided |
| ------------------------------------------------------------ | ------ | ------------------- | -------- |
| `cepsw1studentEN.dta`, `cepsw2studentEN.dta`, `cepsw1parentEN.dta`, `cepsw2parentEN.dta` | CEPS   | As per terms of use | No       |

# Computational requirements

I adopt `R` (version 4.2.0) for all the analyses. This involves the following packages:

- `tidyverse` (version 1.3.1) and `DescTools` (version 0.99.45) for data cleaning

- `fixest` (version 0.10.4) for econometric modeling

- `MatchIt` (version 4.4.0) and `cobalt` (version 4.3.2) for matching

- `modelsummary` (version 1.0.0), `vtable` (version 1.3.3), and `kableExtra` (version 1.3.4) for presenting the results

- `papaja` (version 0.1.0) for typesetting.

## Memory and Runtime 

It takes a few minutes to reproduce the analyses on a standard 2022 desktop machine. The code was last run on a Windows 11 laptop with a 4-core Intel processor.

# Instructions to Replicators

Download the data files referenced above. Then store them in the folder `data/`, in the format that you download them in. Scripts are provided in the same folder. Run `data/Gu-thesis-script.Rmd` to execute all steps in sequence. 

The provided code reproduces 

- [x] All numbers provided in text in the paper
- [x] All tables and figures in the paper

To remake a table or figure, you can locate the specific R chunk by its title. The chunk title corresponds to the Figure/Table numbering in the thesis. 
