# Mankiw, Romer, and Weil (1992) Replication Study: Extended Analysis with Modern Data

## Executive Summary

This study replicates and extends the seminal empirical analysis of Mankiw, Romer, and Weil's (1992) "A Contribution to the Empirics of Economic Growth," reassessing the Solow growth model's ability to explain cross-country differences in living standards. While the original paper used UNESCO-based secondary school enrollment rates as a proxy for human capital over 1960-1985, this study employs an extended time series (1960-2019) and a comprehensive sample of 28 OECD countries, incorporating more sophisticated measures: **Penn World Table (PWT) human capital index (`hc`)** and **World Development Indicators (WDI) working-age population (15-64)**.

Key findings reveal both continuity and important departures from the original results. The textbook Solow model continues to predict the correct directional effects of physical capital accumulation and population growth on income levels, though with reduced explanatory power (R² ≈ 0.225) compared to the original study. The augmented Solow model incorporating human capital significantly improves model fit (R² ≈ 0.483), strongly confirming MRW's central thesis about human capital's decisive role. Most notably, this extended sample exhibits **strong unconditional convergence** (coefficient: -0.6396, p < 0.001), contrasting with the original paper's limited evidence, likely due to the inclusion of successful catching-up economies like Korea, Mexico, Turkey, and Eastern European transition countries.

## 1. Introduction

The Solow growth model, despite its theoretical elegance, faced empirical challenges until Mankiw, Romer, and Weil (1992) demonstrated its explanatory power through careful cross-country analysis. Their augmentation of the basic Solow model with human capital investment resolved the "anomaly" of implausibly high implied capital shares and dramatically improved the model's empirical performance.

This replication study addresses three key questions:
1. Do MRW's core findings remain robust with extended time series data (1960-2019)?
2. How do modern, more sophisticated measures of human capital and labor input affect parameter estimates?
3. What new insights emerge from including countries that experienced remarkable growth transformations over the extended period?

## 2. Data and Methodology

### 2.1 Sample and Time Period

The analysis covers 28 OECD countries from 1960-2019 (T=59 years), significantly extending MRW's original 1960-1985 period. The sample includes: Austria, Belgium, Denmark, France, Germany, Greece, Iceland, Ireland, Italy, Luxembourg, Netherlands, Norway, Poland, Portugal, Spain, Sweden, Switzerland, Turkey, Czech Republic, Hungary, Finland, Korea, Japan, Australia, New Zealand, Canada, USA, and Mexico.

### 2.2 Variable Definitions and Data Sources

**Key improvements over original study:**

| Variable | This Study | Original MRW | Source |
|----------|------------|--------------|---------|
| Income per capita | Real GDP (constant 2017 USD) / Population 15-64 | GDP per working-age population | PWT 10.0 / WDI |
| Human capital | `hc` index (schooling years + returns to education) | Secondary school enrollment rate | PWT 10.0 |
| Labor force | Population ages 15-64 | Working-age population | WDI |
| Investment rate | Share of investment in GDP (`csh_i`) | Investment/GDP ratio | PWT 10.0 |

### 2.3 Model Specifications

**Textbook Solow Model:**
$$\ln(y^*) = \ln A(0) + \frac{\alpha}{1-\alpha} \ln(s) - \frac{\alpha}{1-\alpha} \ln(n+g+\delta)$$

**Human Capital Augmented Model:**
$$\ln(y^*) = \ln A(0) + \frac{\alpha}{1-\alpha-\beta} \ln(s_k) + \frac{\beta}{1-\alpha-\beta} \ln(s_h) - \frac{\alpha+\beta}{1-\alpha-\beta} \ln(n+g+\delta)$$

**Convergence Analysis:**
$$\ln(y_{\text{end}}) - \ln(y_{\text{start}}) = \text{const} + \gamma_1 \ln(y_{\text{start}}) + \text{controls} + \epsilon$$

## 3. Empirical Results

### 3.1 Textbook Solow Model Performance

| Specification | Coefficient | P-value | R² | Implied α |
|---------------|-------------|---------|-----|-----------|
| **Unrestricted Model** | | | **0.225** | **0.526** |
| ln(I/GDP) | 1.110 | 0.055 | | |
| ln(n+g+δ) | -0.464 | 0.503 | | |
| **Restricted Model** | | | **0.210** | **0.456** |
| ln(I/GDP) - ln(n+g+δ) | 0.838 | 0.021 | | |

**Key Findings:**
- Investment rate maintains expected positive effect, though marginally significant
- Population growth coefficient lacks statistical significance (p=0.503)
- R² substantially lower than original study (0.225 vs ~0.59)
- Implied capital share (α ≈ 0.45-0.53) remains above theoretical 1/3, confirming persistent "anomaly"

### 3.2 Human Capital Augmented Model: Dramatic Improvement

| Specification | Coefficient | P-value | R² | 
|---------------|-------------|---------|-----|
| **Unrestricted Model** | | | **0.483** |
| ln(I/GDP) | 0.721 | 0.143 | |
| ln(n+g+δ) | -0.180 | 0.757 | |
| **ln(HC)** | **1.148** | **0.004** | |
| **Restricted Model** | | | **0.397** |
| ln(I/GDP) - ln(n+g+δ) | 0.179 | 0.654 | |
| ln(HC) - ln(n+g+δ) | 0.914 | 0.016 | |

**Implied Parameters (Restricted):**
- α = 0.086 (physical capital share)
- β = 0.437 (human capital share)

**Critical Insights:**
- Human capital coefficient highly significant (p=0.004), confirming MRW's central thesis
- R² doubles compared to textbook model (0.483 vs 0.225)
- Physical and population growth coefficients diminish, suggesting omitted variable bias
- Parameter estimates differ from original (α≈0.29, β≈0.30), indicating sensitivity to data definitions

### 3.3 Convergence Analysis: Strong Evidence for Catch-Up Growth

#### Unconditional Convergence - A New Finding

| Model | ln(Y_start) Coefficient | P-value | R² | Implied λ |
|-------|-------------------------|---------|-----|-----------|
| **Unconditional** | **-0.640** | **<0.001** | **0.606** | **0.0173** |

**Breakthrough Result:** Unlike MRW's limited evidence for unconditional convergence, this extended sample shows **strong, statistically significant unconditional convergence**. This reflects the successful catch-up growth of Korea, Mexico, Turkey, and Eastern European countries included in the expanded OECD sample.

#### Conditional Convergence - Robust Confirmation

| Model | ln(Y_start) | P-value | R² | λ | α (implied) | β (implied) |
|-------|-------------|---------|-----|---|-------------|-------------|
| **Without HC** | -0.635 | <0.001 | 0.740 | 0.0171 | - | - |
| **With HC** | -0.731 | <0.001 | 0.765 | 0.0222 | - | - |
| **Restricted** | -0.707 | <0.001 | 0.728 | 0.0208 | 0.358 | 0.203 |

**Key Observations:**
- Conditional convergence remains robust across all specifications
- Convergence speed increases with human capital inclusion (λ: 0.0171 → 0.0222)
- This contradicts MRW's theoretical prediction of slower convergence in augmented model
- Restricted model parameters align more closely with original findings

## 4. Critical Assessment and Data-Driven Insights

### 4.1 Methodological Improvements and Their Impact

**Human Capital Measurement Enhancement:**
The PWT `hc` index represents a significant advancement over simple enrollment rates, incorporating both years of schooling and returns to education. This quality-adjusted measure better captures human capital's productivity contribution, explaining the improved model performance while generating different parameter estimates.

**Labor Force Definition Refinement:**
Using WDI's 15-64 age population provides a more precise measure of effective labor input compared to broader working-age definitions, potentially affecting convergence speed calculations and parameter estimates.

### 4.2 Sample Composition Effects

The inclusion of successful emerging economies fundamentally alters convergence patterns:

- **Korea (1960 GDP per capita: ~$1,200 → 2019: ~$42,000)**
- **Poland, Czech Republic, Hungary (post-transition growth)**
- **Turkey, Mexico (sustained development)**

These countries' dramatic income increases over 60 years create the strong negative correlation between initial income and subsequent growth, generating unprecedented evidence for unconditional convergence among OECD countries.

### 4.3 Temporal Context: Post-1985 Structural Changes

The extended time period captures fundamental global economic shifts:
- **Globalization acceleration (1990s-2000s)**
- **Technology diffusion and digital revolution**
- **European integration and institutional convergence**
- **Asian economic miracle continuation**

These factors likely enhanced catch-up mechanisms, explaining the robust convergence patterns absent in MRW's original timeframe.

## 5. Model Diagnostics and Robustness

### 5.1 Parameter Stability Analysis

| Parameter | MRW Original | This Study | Difference | Interpretation |
|-----------|--------------|------------|------------|----------------|
| α (physical capital) | ~0.29 | 0.086 | -0.20 | Reduced role of physical capital |
| β (human capital) | ~0.30 | 0.437 | +0.14 | Enhanced human capital importance |
| λ (convergence speed) | ~0.02 | 0.017-0.022 | Comparable | Consistent convergence rate |

### 5.2 Specification Testing

- **Restriction tests:** Generally support model constraints (F-test p-values > 0.05)
- **Residual diagnostics:** No significant heteroscedasticity or autocorrelation
- **Outlier analysis:** Results robust to individual country exclusion

## 6. Economic Interpretation and Policy Implications

### 6.1 The Continued Relevance of Solow Framework

Despite nearly three decades since MRW's publication, the Solow growth model framework remains empirically relevant:

1. **Physical capital accumulation** maintains its positive income effect, though its relative importance may have declined
2. **Human capital investment** emerges as even more critical in the modern economy
3. **Convergence mechanisms** appear stronger, potentially due to enhanced technology transfer and institutional learning

### 6.2 New Insights for Growth Policy

**Human Capital Priority:** The strong and consistent significance of human capital across all specifications reinforces education and skill development as fundamental growth drivers.

**Convergence Opportunities:** The evidence for unconditional convergence among OECD countries suggests that appropriate institutions and policies can enable sustained catch-up growth even for initially poor countries.

**Diminished Physical Capital Role:** The reduced implied physical capital share may reflect the growing importance of intangible assets, knowledge, and services in modern economies.

## 7. Limitations and Future Research Directions

### 7.1 Data Definition Sensitivity

The substantial differences in parameter estimates highlight the importance of variable definitions. Future research should systematically compare:
- UNESCO enrollment rates vs. PWT human capital index
- Various labor force definitions
- Alternative investment measures

### 7.2 Sample Selection and Generalizability

While the OECD sample provides institutional homogeneity, extending analysis to broader country samples would test generalizability. The strong convergence findings may reflect OECD-specific factors rather than universal growth patterns.

### 7.3 Structural Break Analysis

The 60-year time span likely encompasses multiple structural breaks. Period-specific analysis (1960-1985 vs 1986-2019) could identify how global economic changes affected growth model parameters.

## 8. Conclusion

This replication study confirms the continued empirical relevance of the Solow growth model while revealing important new insights. The augmented model with human capital remains superior to the textbook version, with human capital's role potentially even more critical in the modern economy. Most significantly, the strong evidence for unconditional convergence among OECD countries provides new support for catch-up growth possibilities.

The findings emphasize three key lessons for growth economics:

1. **Data definitions matter profoundly** for parameter estimates and policy conclusions
2. **Sample composition and time periods critically affect convergence patterns**
3. **The Solow framework, properly augmented, remains a powerful tool for understanding cross-country growth differences**

These results validate MRW's core insights while demonstrating how extended data and refined measurements continue to enhance our understanding of the growth process. The evidence suggests that with appropriate policies and institutions, countries can achieve sustained convergence toward higher living standards—a fundamentally optimistic conclusion for development economics.

---

*This analysis replicates Mankiw, Romer, and Weil (1992) using Python/statsmodels with data from Penn World Table 10.0 and World Development Indicators. Full replication code and data available at: https://github.com/ben10js/MRW_Replication*