# growth-mindset-causal-inference
Causal inference project analyzing growth mindset interventions using OLS, IPW, AIPW, and propensity score stratification in R.

# Unlocking Student Potential: A Causal Analysis of Growth Mindset Interventions
This repository contains the research poster and source code for my project at Rutgers University.  
The project applies **modern causal inference techniques** to evaluate the impact of growth mindset interventions on student achievement.

---

## Dataset Description

The original experiment randomly assigned **10,000 students** to treatment and control groups across **76 U.S. public high schools**.  

For this project, a **synthetic dataset** was generated to mimic the structure of the original study, but it should be considered **observational** (not experimental).  

### Covariates

- **Student-level**  
  - `selfrpt`: Student’s self-reported expectations for success in the future (proxy for prior achievement, measured pre-treatment)  
  - `race`: Student race/ethnicity *(categorical)*  
  - `gender`: Student’s identified gender *(categorical)*  
  - `fgen`: Indicator for first-generation college student *(binary)*  

- **School-level**  
  - `urban`: Urbanicity of the school *(categorical)*  
  - `mindset`: School-level mean of students’ fixed mindsets, measured prior to treatment  
  - `test`: School-level achievement (test scores & college preparation of prior four cohorts)  
  - `sch_race`: Racial/ethnic minority composition  
  - `pov`: Poverty concentration (% of students below the federal poverty line)  
  - `size`: Total number of students across all four grade levels  

### Treatment & Outcome
- `Z`: Treatment indicator (whether the student received the growth mindset nudge-like intervention)  
- `Y`: Continuous measure of student achievement  

### Goal
The objective of this project is to **estimate the average treatment effect (ATE)** of the growth mindset intervention on student achievement — i.e., the causal effect of `Z` on `Y`.  

---

## Highlights
- Built a **synthetic observational dataset** modeled on the National Study of Learning Mindsets.
- Applied **OLS, Inverse Probability Weighting (IPW), Augmented IPW (AIPW), and Propensity Score Stratification**.
- Verified **covariate balance** using love plots and density plots.
- Estimated **Average Treatment Effect (ATE)** consistently across methods (~0.41–0.46).
- Produced an interactive HTML poster and polished academic PDF.

---

## Repository Contents
- `Final_Poster.Rmd` — R Markdown source file.  
- `Final_Poster.html` — Interactive version of the poster.  
- `Stat_Poster.pdf` — Final poster for presentation.  
- `data.csv` — Synthetic dataset or script to generate data.  
- `ATE_results.png` — ATE results.

---

## Skills Demonstrated
- **Causal Inference**: IPW, AIPW, Propensity Scores, Stratification, Trimming  
- **Statistical Modeling**: Regression Adjustment, Estimator Comparison  
- **Programming in R**: tidyverse, cobalt, ggplot2  
- **Data Visualization**: Covariate balance plots, outcome distributions, ATE comparisons  
- **Reproducible Research**: RMarkdown, GitHub hosting  

---

## Preview
Example: Estimated treatment effect using multiple causal methods.  
![ATE Results](ATE_results.png)

---

## How to View 
- [Download PDF Poster](./Stat_Poster.pdf)
- You can explore the html version of this project here:
[**View html**](https://chimbililohith.github.io/growth_mindset/) 

---

*Project completed as part of my **M.S. in Data Science at Rutgers University**.*
