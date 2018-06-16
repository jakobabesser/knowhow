## Empirical Research Process

* operationalization
 * how to measure constructs?

* data preparation
 * integrate data to scales
 * interpolate missing data

## Research Design

* empirical study
 * test phenonenon / hypothesis / theory
 * or: replication study
* experimental study / true experiment
 * assign participants to conditions randomly!
* frequency of measurements
 * cross-sectional design
 * repeated-measurement design
  * confront participants with every conditions

* number of research objectives
 * sample study (only part of targeted population)

## Experimental Design

* experimental manipulation of treatment (independent variables)
* measurement of dep. vars. (effects)

* causal influences
 * internal validity
  * results allow for causal interpretations of effects
  * exclusion of alternative explanations
  * confounder (influences on dependent variable beyond independent variables)
     * randomizations, standardization, double-blind trials

== Effect size & power analysis ==

* significance test
 * null-hypothesis significance testing (NHST) will always lead to significant results
if n is high enough even if it is of no practical relevance
   * p values depend among effect also on the sample size -> problematic
* better
 * report stat. significance (test statistics, p-value) & standardized effect size
 * absolute effect sizes are hard to compare across studies (mean differences ...)
 * e.g. Cohen's d effect sizes

* another problem (NHST)
 * effect of practical relevance without statistical significance?
 * => possible if n is low
 * power = prob. to find significant population effect
 * if results are non-significant (n too small) but have effect size -> report but also do power analysis
* 80% of power minimum
 * power increases with sample size, population effect, significance level
   * controllable is only sample size!
* power analysis : g*power

## Data analysis

* descriptive statistics
 * report sample data (social demographics, additional variables that might be confounders)
 * mean, variance, correlations, frequencies
* inferential statistics
 * inference from sample data to population effects
 * parameter estimation (point & interval estimation, e.g. confidence intervals)
 * testing hypothesis, significance tests

* two-group (t-test): control vs. experimental group

## Chose test

* type of hypothesis
 * difference, correlation, change (over time, often same participants before / after)
* levels of measurements
 * nominal (eye color) -> categories
 * ordinal (level of edu) -> ranking
 * interval (year) -> same difference between items
 * ratio (age) -> includes zero

### Example: two groups
* ex: improved spatial orientation task performance with / without spatial audio
* test of differences
* student t-tests
 * require normal distribution of DV, equal / similar variances
 * Levene's test for equality of variances -> might require df correction
* Mann-Whitney U-Test = non-parametric alternative
* weighting might be required if classes are heavily imbalanced!

* parametric versions include more variance as non-parametric also work with nominal / ordinal

* independent samples = different participants for both stimuli
* dependent samples = same participants in both conditions
 * need fewer samples this way
 * need to control for learning effect by randomize order of presentation

## One-way / one-factor design

* one-way univariate ANOVA (uni = 1, variate = dependent variable)
 * anova less stable than t-test
 * requirements, DV = interval / ratio, DV normal dist., N > 20 per cell
 * Kruskall-Wallis-test = non-parametric alternative
* for multiple classes -> report table with all combinations and highlight significant ones
