# NHL Player Development Paths: A Causal Inference Analysis

**Carnegie Mellon University | M.S. in Statistical Practice Capstone | Spring 2021**

**Client:** Pittsburgh Penguins  
**Faculty Advisor:** Brian Macdonald  
**Team:** Minyue Fan, Steve Kim, Kexiong Shen, Linda Yang

## Overview

This project was conducted as part of Carnegie Mellon University's Master of Science in Statistical Practice (MSP) capstone program in collaboration with the Pittsburgh Penguins.

The objective was to investigate whether the developmental paths taken by hockey prospects causally influence their future success in the National Hockey League (NHL). Although players who enter the NCAA historically exhibit higher NHL success rates, these differences may reflect selection bias, as stronger prospects are more likely to enter the NCAA in the first place.

We applied causal inference methods to distinguish the effect of developmental league selection from differences in players' underlying characteristics and abilities.

## Research Problem

The analysis focused on players who competed in the United States Hockey League (USHL) at age 18 and subsequently either transitioned to the NCAA or remained in the USHL at age 19.

- **Treatment:** Transitioning to the NCAA versus remaining in the USHL.
- **Outcome:** Average number of NHL games played per season.
- **Confounders:** Pre-treatment player characteristics, including draft value, goals, assists, plus-minus rating, penalty minutes, height, and weight.

The primary research question was whether transitioning to the NCAA improves subsequent NHL performance after accounting for observable differences between players.

## Methodology

### 1. Exploratory Analysis and Markov Models

Analyzed player development trajectories across leagues using historical player performance and biographical data from 2000–2020.

The team used alluvial visualizations and Markov chain models to examine league transitions and identify patterns in players' progression toward the NHL.

### 2. Propensity Score Weighting

Estimated treatment assignment probabilities using logistic regression based on pre-treatment player characteristics.

Applied propensity score weighting to adjust for observed differences between players entering the NCAA and those remaining in the USHL.

The analysis included:

- Constructing player-level features and standardized performance metrics.
- Estimating propensity scores using logistic regression.
- Comparing inverse-probability weighting, alternative weighting specifications, and propensity score matching.
- Evaluating covariate balance and estimating treatment effects using weighted regression.
- Conducting separate analyses for forwards and defensemen.

### 3. Bayesian Additive Regression Trees (BART)

The team also employed Bayesian Additive Regression Trees to estimate treatment effects while flexibly modeling nonlinear relationships between player characteristics, developmental league, and NHL performance.

BART estimates were compared with propensity score weighting results to assess the consistency of the findings.

## Key Findings

- Players transitioning to the NCAA exhibited higher unadjusted NHL success rates than those remaining in the USHL.
- After adjusting for observed differences in player characteristics, the estimated effects of transitioning to the NCAA were substantially smaller and not statistically significant.
- Both propensity score weighting and BART analyses suggested that developmental league choice in the first year following draft eligibility was not a significant predictor of future NHL games played.
- Draft value emerged as an important predictor of subsequent NHL performance.

These findings suggest that observed differences in NHL outcomes between developmental leagues may largely reflect differences in player characteristics rather than the developmental path itself.

## My Contributions

My primary contribution to the team project was the propensity score analysis, documented in the accompanying R Markdown file.

This work included data preparation, construction of player-level covariates, propensity score estimation, implementation and comparison of weighting methods, covariate balance assessment, and treatment-effect estimation through weighted regression.

## Repository Contents

- **Pittsburgh_Penguins_Project.pdf:** Final capstone report describing the research problem, methodology, results, and conclusions.
- **prop_weighting.Rmd:** R Markdown implementation of the propensity score analysis, including data preparation, weighting, matching comparisons, and outcome modeling.
- **Final Progress Report.pdf:** Final presentation summarizing the team's analysis and findings.

## Implementation

**Language:** R

**Methods:** Propensity score weighting, logistic regression, weighted linear regression, propensity score matching, and Bayesian Additive Regression Trees.

The included R Markdown file documents the propensity score component of the analysis. It references external player-level datasets that are not included in this repository.

