# Microbiota adaptation review
This is the data and code repository of the quantitative study of microbe-driven acclimation and adaptation in wild vertebrates conducted in 2023. The associated manuscript is currently under review:

Martin-Bideguren G, Razgour O, Alberdi A. 2023. **Quantitative synthesis of microbe-driven acclimation and adaptation in wild vertebrates**. Submitted.

In the following, the main steps carried out in the study are listed, with references to data files, results and figures.

## 1. Data search
We conducted a literature search for articles published between 2016 and 2023 in Scopus (Elsevier) and Web of Science (Clarivate) databases. The data  included in this repository and the associated manuscript was fetched on the 1st of June 2023. Publications where searched using the following string:

> (wild*) AND (animal*) AND (adapt*) AND (“gut microbiota” OR “gut microbiome” OR “intestinal microbiota” OR “intestinal microbiome” OR “GUT microbiota” OR “GUT microbiome”)

The resulting tables can be found in the data folder:
- **Scopus:** [Scopus_20230601.csv](data/Scopus_20230601.csv)
- **Web of Science:** [WOS_20230601.csv](data/WOS_20230601.csv)

## 2. Data preprocessing
The search results were downloaded in tabular format, and subsequently merged and filtered to obtain the definitive list of 1974 publication that was used for downstream analyses. The code used for these preprocessing steps is available in **[1-data_preprocessing.Rmd](1-data_preprocessing.Rmd)**.

The resulting table containing the 1974 publications can be found in the data folder:
- **All preprocessed data:** [all_20230601.csv](data/all_20230601.csv)

## 3. Study screening
The 1974 studies were manually screened to analyse whether they met the following inclusion criteria:
1. The study analyses the gut microbiota
2. The study revolves around or touches upon environmental adaptations
3. The study focused on wild vertebrates and iv) is based on empirical data.

This second filtering step yielded 109 studies, which were scrutinised in detail to assign performance scores.

## 4. Study scoring
The performance of studies to address the microbial adaptive contribution hypothesis was assessed considering ten criteria clustered into three domains:
- Experimental design
- Methodological resolution
- Reproducibility.

For each one of these 10 criteria, a quantitative value ranging 0-1 was assigned to each of the 109 studies. The values can be found in the file [data/scores.tsv](data/scores.tsv).

## 5. Criteria weighing
Each of the ten analysed criteria was given a different weight to obtain the overall performance scores for each publication through weighted average calculation. To minimise subjectivity, we requested 8 independent experts to assign relevance values to each of the ten criteria. The weighs provided by the experts are shown in [data/weights.tsv](data/weights.tsv).

## 6. Study analysis
Using the above data files, we conducted the statistical analyses and visualisations that are compiled in the code file **[2-data_analysis.Rmd](2-data_analysis.Rmd)**, and generated the results and figures shown in the rendered markdown document **[microbiota_adaptation_review.pdf](microbiota_adaptation_review.pdf)**.
