# Task 07 – Standard Deviation

## Problem Statement

Given test scores: 88, 92, 79, 85, 95, 81, 86, 90, 83, 77, 89. 
Calculate the mean and sample standard deviation. If the highest and lowest scores are removed, what are the new mean and standard deviation?

## Theory

The sample mean $\bar{x}$ and sample standard deviation $\sigma$ (or $s$) are calculated as:

$$
\bar{x} = \frac{1}{N} \sum_{i=1}^N x_i
$$

$$
\sigma = \sqrt{\frac{1}{N-1} \sum_{i=1}^N (x_i - \bar{x})^2}
$$

## Step-by-Step Solution

### Initial Data Set ($N = 11$)

Scores: 77, 79, 81, 83, 85, 86, 88, 89, 90, 92, 95.

Calculate the sum:

$$
\sum x_i = 945
$$

Calculate the mean:

$$
\bar{x} = \frac{945}{11} \approx 85.91
$$

Calculate the sum of squared deviations $\sum (x_i - \bar{x})^2$:

$$
(77-85.91)^2 + (79-85.91)^2 + \dots + (95-85.91)^2 \approx 310.91
$$

Calculate the standard deviation:

$$
\sigma = \sqrt{\frac{310.91}{11 - 1}} = \sqrt{31.091} \approx 5.58
$$

### Modified Data Set ($N = 9$)

Remove highest (95) and lowest (77).
Remaining scores: 79, 81, 83, 85, 86, 88, 89, 90, 92.

Calculate the new sum:

$$
\sum x_i = 945 - 95 - 77 = 773
$$

Calculate the new mean:

$$
\bar{x}_{new} = \frac{773}{9} \approx 85.89
$$

Calculate the new sum of squared deviations:

$$
(79-85.89)^2 + \dots + (92-85.89)^2 \approx 148.89
$$

Calculate the new standard deviation:

$$
\sigma_{new} = \sqrt{\frac{148.89}{9 - 1}} = \sqrt{18.61} \approx 4.31
$$

## Final Result

* Initial: Mean = $85.91$, Std Dev = $5.58$
* Modified (outliers removed): Mean = $85.89$, Std Dev = $4.31$

## Interpretation

Removing the extremes barely changed the mean (from 85.91 to 85.89) because the highest and lowest scores were symmetrically distant from the center. However, the standard deviation dropped significantly (from 5.58 to 4.31), reflecting a much tighter clustering of the remaining data points.
