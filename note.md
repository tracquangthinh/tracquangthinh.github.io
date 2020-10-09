This is a note what I found and read about statistical methods and my relevant personal questions, maybe other topics sometimes.
I try to summarize what I have understood but life is hard, thus many summaries here are totally wrong. If you see some topics lack of their summary,
it means I haven't read it :)).

#### 9th October 2020
- [Why using Welch's t-test (unequal variance t-test) instead of t-test?](https://daniellakens.blogspot.com/2015/01/always-use-welchs-t-test-instead-of.html)
  - **Summary**: The distribution of p-values of Welch's t-test is uniform while the one of t-test is right skew
- [How to use Welch's t-test?](https://academic.oup.com/beheco/article/17/4/688/215960)
- [Do we need normality for t-test?](https://thestatsgeek.com/2013/09/28/the-t-test-and-robustness-to-non-normality/)
  - **Summary**: t-test compare *means* of groups. when the sample size becomes larger enough (-> infinite), the distribution of means becomes "likely" normal.
  It means we can conduct t-test no matter what kind of distribution our data come from.
- [t-test, ANOVA is special cases of linear regression! Really?](https://lindeloev.github.io/tests-as-linear/#42_paired_samples_t-test_and_wilcoxon_matched_pairs)
  - **Summary**: Quite long to summarize all methods. But remember one sample t-test (*mean of a group = a number?*) equals to y = beta0. The idea here is that
  we can calculate p-value and confident interval (CI) for intercept *beta0* (like *lm* function from R) and *beta0* is the mean of the group (using OLS). Thus we can
  have p-value and CI of *y_hat = a number* by using linear regression or t-test and linear regression provide same results.
  
#### 10th October 2020
- [Bessel's correction](https://en.wikipedia.org/wiki/Bessel%27s_correction)
  - **Summary**: Why do we divive *n-1* when calculating population variance? That's because the population variance is estimated based on the sample variance
  but this estimation is biased. Hence we need *n-1* as the correction.
