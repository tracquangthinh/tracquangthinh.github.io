This is a note what I found and read about statistical methods and my relevant personal questions, maybe other topics sometimes.
I try to summarize what I have understood but life is hard, thus many summaries here maybe totally wrong. If you see some topics lack of their summary,
it means I haven't read it :)).

#### 9th October 2020
- [Why using Welch's t-test (unequal variance t-test) instead of t-test?](https://daniellakens.blogspot.com/2015/01/always-use-welchs-t-test-instead-of.html)
  - **Summary**: The distribution of p-values of Welch's t-test is uniform while the one of t-test is right skew
- [How to use Welch's t-test?](https://academic.oup.com/beheco/article/17/4/688/215960)
- [Do we need normality for t-test?](https://thestatsgeek.com/2013/09/28/the-t-test-and-robustness-to-non-normality/)
  - **Summary**: t-test compare *means* of groups. when the sample size becomes larger enough (-> infinite), the distribution of means becomes "likely" normal.
  It means we can conduct t-test no matter what kind of distribution our data come from.
  
#### 10th October 2020
- [Bessel's correction](https://en.wikipedia.org/wiki/Bessel%27s_correction)
  - **Summary**: Why do we divive *n-1* when calculating population variance? That's because the population variance is estimated based on the sample variance
  but this estimation is biased. Hence we need *n-1* as the correction.
- [t-test, ANOVA is special cases of linear regression! Really?](https://lindeloev.github.io/tests-as-linear/#42_paired_samples_t-test_and_wilcoxon_matched_pairs)
  - **Summary**: This is a painful topic for me to understand the concept at least. Assuming we need to compare means of 3 groups. It's not easy to see the connection between ANOVA and Linear Regression (LR).
  First, a good new is that we can calculate Confident Interval (CI) for the slope (coeffient) and the intercept of LR: ![y=\beta_0 + \beta_1.x](https://latex.codecogs.com/svg.latex?y=\beta_0+\beta_1*x_1+\beta_2*x_2). The basic idea is using dummy coding *0* or *1* for *x*. For example, if *x* comes from group *2*, *x = [0, 1, 0]* and then ![y=\beta_0 + \beta_1](https://latex.codecogs.com/svg.latex?y=\beta_0+\beta_1) is the average of group *2*. Similarity, ![y=\beta_0](https://latex.codecogs.com/svg.latex?y=\beta_0) is the average of group *1* and ![y=\beta_0 + \beta_2](https://latex.codecogs.com/svg.latex?y=\beta_0+\beta_2) is the average of group *3*. So no difference between 3 groups means ![y=\beta_0](https://latex.codecogs.com/svg.latex?y=\beta_0). *lm* function in R provides F-statistic and p-value to test this hypothesis [F-test in Linear Regression](https://blog.minitab.com/blog/adventures-in-statistics-2/what-is-the-f-test-of-overall-significance-in-regression-analysis#:~:text=In%20general%2C%20an%20F%2Dtest,form%20of%20the%20F%2Dtest)

#### 21st October 2020
- [Wilk's theorem](https://stephens999.github.io/fiveMinuteStats/wilks.html)
  - **Summary**: Likelihood ratio follows chi-square distribution when the number of sample is large enough.
- [GLM Deviance](https://bookdown.org/egarpor/PM-UC3M/glm-deviance.html)
  - **Summary**: The generalized definition of Sum Squared Error(SSE). It's also the foundation of R2 or mainly using to compare models (In all likelihood, p.168)

#### 26th October 2020
- [What's a good scale, original or log(y), p.22, GLM book, Nelder](http://www.utstat.toronto.edu/~brunner/oldclass/2201s11/readings/glmbook.pdf)
  - **Summary**: For classical linear model, a good scale should have constancy of variance, approximate normality of errors, additivity of effects.
- [Sufficient statistic](https://en.wikipedia.org/wiki/Sufficient_statistic)
  - **Summary**: When using likelihood-based inference, two sets of data yielding the same value for the sufficient statistic T(X) will always yield the same inferences about θ
  
#### 8th November 2020
- [Empirical distribution](https://en.wikipedia.org/wiki/Empirical_distribution_function)
  - **Summary**: Observed distribution. In R, using ecdf to calculate empirical cummulative distribution function and then p-value.
  
#### 9th November 2020
- [Boostrapping for empirical p-value](https://janhove.github.io/teaching/2016/12/20/bootstrapping)
  - **Summary**: When you want to calculate p-value of a object belonging to a set but your facing problem is the small sample size. Boostraping should be your solution!

#### 26th November 2020
- [Why we need a canonical (natural) parameter in the exponential family?](https://www.quora.com/What-is-a-natural-parameter%E2%80%9D-of-an-exponential-family-and-why-is-it-helpful)
  - **Summary**: Natural parameter is just like its name, belongs to R instead of a range. And easier for derivatives.

#### 19th August 2021
- [When should we use log-scale?](https://stats.stackexchange.com/questions/27951/when-are-log-scales-appropriate)
  - **Summary**: Using log-scale for visualization is not simple as stretching the graph to help our eyes. Log-scale should be used when the data follow the log-scaled distribution (e.g drug concentrations) or for timeseries problems.
- [chi-square can be used only for counts data](#)
  - **Summary**: Never use the chi-square formula to calculate some kind of errors... 
