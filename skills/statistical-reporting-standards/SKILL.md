---
name: statistical-reporting-standards
description: Detailed statistical reporting checklist (APA 7th edition standard) - universal checklist (descriptives, effect size, CI, statistical power, missing data, assumption testing), per-method checklists (t-test, ANOVA, regression, SEM, HLM, chi-square, non-parametric), APA number/symbol formatting, p-hacking/HARKing/GRIM/GRIMMER red flags, and a statistical-completeness scoring rubric. Use in Layer 3 (Evidence) when assessing a quantitative manuscript's Methods/Results section - deepens scientific-review's MFE Checklist.
---

# Statistical Reporting Standards

An operational checklist for assessing whether a quantitative
manuscript's statistical reporting is complete and correct, per the
APA 7th edition standard. Deepens `scientific-review`'s MFE Checklist -
use this skill when you need line-by-line statistical rigor, not just
the general "does the statistics look adequate?" check.

## 1. Universal checklist (every quantitative article)

- **Descriptives**: mean (*M*) and standard deviation (*SD*) always
  together (never *SD* swapped for standard error *SE* without saying
  so); total and per-group *N*; range or IQR; frequency (*f*) and
  percentage for categorical variables - never just the percentage.
- **Effect size (mandatory per APA 7th ed.)**: every statistical test
  needs to come with an effect size, not just a *p*-value. Metric by
  method: *t*-test → Cohen's *d* (small/medium/large: 0.2/0.5/0.8);
  ANOVA → eta²/partial eta² (.01/.06/.14); correlation → *r*
  (.10/.30/.50); regression → R²/*f*² (*f*²: .02/.15/.35); chi-square →
  Cramer's *V*/*phi* (.10/.30/.50); odds ratio → OR (1.5/2.5/4.3). The
  number alone isn't enough - it needs a magnitude interpretation.
- **Confidence interval**: every effect size and key estimate should
  report a 95% CI in the format `[lower bound, upper bound]`; interpret
  what the CI says about precision, not just whether it crosses zero.
- **Statistical significance**: exact *p*-value (`p = .032`, not just
  `p < .05`); `p < .001` only when very small, never `p = .000`; alpha
  level declared a priori; correction for multiple comparisons
  (Bonferroni/Holm/FDR); non-significant results reported in full,
  never hidden.
- **Statistical power**: a priori power analysis (target >= .80,
  assumed effect size, alpha, required N), source of the assumed effect
  size, tool used (G*Power, the `pwr` package, etc.); for non-significant
  results, discuss Type II error risk.
- **Missing data**: amount and proportion per variable; mechanism
  discussed (MCAR/MAR/MNAR, not assumed); method stated (listwise/
  pairwise/multiple imputation/FIML); ideally a sensitivity analysis
  comparing methods.
- **Assumption testing**: normality (Shapiro-Wilk/K-S/Q-Q), homogeneity
  of variance (Levene), linearity, independence (Durbin-Watson or a
  design-based justification), multicollinearity (VIF),
  residual normality/homoscedasticity (regression) - "N > 30 so I don't
  need to test" is not a valid justification.

## 2. Per-method checklists (apply whichever fits the design)

- **t-test**: statistic `t(df) = X.XX, p = .XXX`; independent vs.
  paired chosen correctly; Cohen's *d* (or paired *d_z*); assumptions
  tested; Welch correction if variances are unequal; directionality
  (one/two-tailed) justified a priori.
- **ANOVA**: `F(df1,df2) = X.XX, p = .XXX`; eta²/partial eta²/omega²;
  post hoc when the main effect is significant (Tukey/Bonferroni/
  Games-Howell); interactions interpreted in factorial designs;
  sphericity (Mauchly + Greenhouse-Geisser/Huynh-Feldt correction) for
  repeated measures.
- **Linear regression**: R²/adjusted R²/model F test; full coefficient
  table (*B*, *SE*, *beta*, *t*, *p*, 95% CI); VIF; residual diagnostics
  (normality, homoscedasticity, outliers via Cook's D); variable-selection
  method justified.
- **Logistic regression**: model fit (Hosmer-Lemeshow/-2LL/Nagelkerke
  R²); coefficients (*B*, *SE*, Wald, OR, 95% CI of the OR);
  classification accuracy/sensitivity/specificity/AUC; the EPV rule
  (10-20 events per predictor).
- **SEM**: N >= 200 (or 5-10x the estimated parameters); **at least 4**
  simultaneous fit indices (CFI/TLI >= .95 good, >= .90 acceptable;
  RMSEA <= .06 good with 90% CI; SRMR <= .08; chi²/df <= 3); standardized
  factor loadings >= .50; CFA before SEM (two-step approach);
  reliability/validity (CR >= .70, AVE >= .50).
- **Chi-square**: `chi²(df, N=XX) = X.XX, p = .XXX`; Cramer's V (>2x2)
  or phi (2x2); expected frequency >= 5 in every cell (otherwise, Fisher's
  exact test); standardized residuals when significant.
- **Non-parametric**: explicit justification for not using the
  parametric test; correct test (Mann-Whitney/Wilcoxon/Kruskal-
  Wallis/Friedman); effect size (*r* = Z/√N for Mann-Whitney).

## 3. APA 7th edition formatting (numbers and symbols)

- No leading zero for statistics that can't exceed 1.0 (`r = .45`, not
  `r = 0.45`) - applies to *r*, *R*, proportions/p-value, Cramer's V,
  phi, eta², R², standardized beta.
- Leading zero for statistics that can exceed 1.0 (`M = 0.75`) -
  applies to M, SD, B, Cohen's d, t, F, chi².
- Generally two decimal places; p-value with 2-3 places (`p = .032`,
  never `p = .0321`); percentages with 0-1 decimal place.
- Italic: *M*, *SD*, *SE*, *N*/*n*, *t*, *F*, *p*, *r*, *R*, *z*, *d*,
  *B*, *beta*, *chi²*. Not italic: df, SS, MS, OR, CI, VIF, AIC, BIC,
  CFI, TLI, RMSEA, SRMR, ICC.
- Three-line table (above the header, below the header, bottom of the
  table) - no vertical lines; numbers right-aligned, decimals aligned.

## 4. Statistical red flags (warning signs, not an automatic verdict)

These are triggers to investigate further, not an automatic
condemnation - but once confirmed, they become a real finding in the
report.

- **P-hacking**: many *p*-values clustered at .04-.05; selective
  reporting (only significant results appear); analysis strategy not
  declared a priori; "discovered" post hoc subgroups; flexible sample
  size with no stopping rule; mass outlier exclusion with no clear
  criterion.
- **HARKing** (Hypothesizing After the Results are Known): 100% of
  hypotheses confirmed with no exception; literature review clearly
  built post hoc; a hypothesis's direction changed without
  acknowledgment.
- **Missing effect size/CI**: conclusion based only on a p-value; CI
  absent or extremely wide; reported effect size inconsistent with what
  the raw data would allow you to calculate.
- **Sample**: no power analysis; N < 10x predictors in regression;
  large, unexplained sample attrition.
- **Uncorrected multiple comparisons**: multiple t-tests instead of
  ANOVA for 3+ groups; multiple dependent variables tested separately
  without Bonferroni/FDR; testing several models and reporting only
  "the best one".
- **Assumptions**: testing absent; violation reported but the original
  analysis kept anyway; high VIF (>10) with no action taken.
- **Signs of numerical inconsistency** (the most serious level, can
  indicate error or fabrication, not just incomplete reporting):
  - **GRIM**: for discrete-scale data, the reported mean needs to be
    algebraically reachable given the stated N and precision - if it
    isn't, that's a real inconsistency signal (Brown & Heathers, 2017).
  - **GRIMMER**: GRIM's extension to standard deviation - same
    principle, checking whether the reported SD is reachable given the
    mean and N.
  - `p` incompatible with the reported statistic/df (doesn't match any
    plausible tail reading).
  - df inconsistent with the N reported in the text.
  These four should only be raised when you (or the user) can actually
  recompute and check - never claim "GRIM inconsistency" by intuition
  without doing the math.

## 5. Statistical-reporting completeness rubric (0-100)

| Dimension | Weight | Full-score criterion |
|---|---|---|
| Complete descriptives | 15% | M, SD, N, range present |
| Effect size reported | 20% | Every test comes with an effect size |
| Confidence interval | 15% | Key estimates include a CI |
| Assumption testing | 15% | Every relevant assumption tested |
| Statistical power | 10% | Complete a priori power analysis |
| Missing data | 10% | Amount + handling method reported |
| APA formatting | 10% | Symbols, decimals, tables compliant |
| No red flags | 5% | No red flag from Section 4 detected |

Bands: 90-100 exemplary; 70-89 adequate (minor omissions); 50-69 needs
improvement (significant omissions); 30-49 inadequate; 0-29 insufficient
to support the conclusions.

## 6. Recommended checking order

1. Does the research question match the chosen analysis method?
2. Is assumption testing reported?
3. Universal checklist (section 1), item by item.
4. Method-specific checklist (section 2).
5. Red-flag scan (section 4).
6. APA formatting (section 3).
7. Completeness score (section 5).

## Relation to the rest of the pipeline

Use this skill in `scientific-boss` (Layer 3 - Evidence), as a
deepening of the already-existing MFE Checklist - the MFE Checklist
covers methodology/figures more broadly, this skill covers statistical
reporting line by line. It doesn't replace the rigor rules (em dash,
citations, limitations, funding, AI) or the Data Integrity Principle -
it specifically complements the numerical check.
