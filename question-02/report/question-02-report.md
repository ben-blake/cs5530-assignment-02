## Question 2: Diabetes Data Analysis

This analysis focused on comparing sample statistics with population parameters using the Diabetes dataset.

### Part A: Random Sampling (n=25)

A random sample of 25 observations was drawn (seed=42) to estimate Glucose levels.

- **Mean Glucose**:
  - Sample: **116.64**
  - Population: **120.89**
  - _Observation_: The sample mean slightly underestimates the population mean but is reasonably close.
- **Max Glucose**:
  - Sample: **183**
  - Population: **199**
  - _Observation_: The sample maximum is lower than the population maximum, which is expected in smaller samples as extreme values are less likely to be captured.

### Part B: Percentiles (BMI)

I compared the 98th percentile of BMI for the sample and the population.

- **Sample 98th Percentile**: **40.25**
- **Population 98th Percentile**: **47.53**
- _Observation_: The sample significantly underestimates the 98th percentile. Percentiles, especially extreme ones like the 98th, are highly sensitive to sample size. A small sample (n=25) often fails to capture the extreme tail of the distribution accurately.

### Part C: Bootstrap Analysis (500 samples of n=150)

Bootstrap resampling was used to create robust estimates for Blood Pressure statistics.

- **Mean Blood Pressure**:

  - Bootstrap Average: **69.18**
  - Population Mean: **69.11**
  - _Observation_: The bootstrap mean is extremely close to the true population mean, demonstrating the central limit theorem in action.

- **Standard Deviation**:

  - Bootstrap Average: **19.07**
  - Population Std: **19.36**
  - _Observation_: The bootstrap standard deviation is very close to the population standard deviation, indicating that the variability in the samples mirrors the population.

- **98th Percentile**:
  - Bootstrap Average: **97.90**
  - Population 98th Percentile: **99.32**
  - _Observation_: The bootstrap estimate for the 98th percentile is much closer to the population parameter compared to the single small sample in Part B. Increasing the sample size (n=150) and using bootstrapping provided a much better estimate of the tail of the distribution.

### Conclusion

My analysis demonstrates that while small single samples can provide rough estimates of central tendency (mean), they often fail to capture the extremes (max, high percentiles). Bootstrapping with larger sample sizes provides very accurate estimates for both central tendency and variability, closely approximating the true population parameters.
