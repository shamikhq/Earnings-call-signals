## Primary Specification

**Research question:** Does negative or uncertain language in management's Q&A answers on earnings calls predict subsequent stock returns, beyond what earnings surprise and known return predictors already explain?

**Hypothesis:** Firms whose management uses more negative and uncertain language in Q&A answers earn lower returns over the month following the call. In other  words, the relationship between negative or uncertain language and subsequent returns is expected to be negative.

**Method:** Fama-MacBeth cross-sectional regression. For each month, the following-month stock return is regressed across firms on the language measure and the controls below. The resulting estimates are then averaged over time.

**Outcome:** Each firm's stock return from the second trading day through the twenty-first trading day after the call (about one month), starting after the announcement reaction. For calls that occur after the market close, the first trading day is the next trading day.

**Language measure:** The share of words in management's Q&A answers that are negative or uncertain according to the Loughran-McDonald financial dictionary. Analyst questions are excluded, and the measure is standardized across firms within each period.

**Controls:**
- Earnings surprise: actual earnings per share relative to Bloomberg analyst consensus, standardized
- Announcement reaction: the stock's return over the first two trading days around the call
- Firm size: market capitalization measured before the call
- Book-to-market ratio: using book equity from the latest filing available at the call date
- Market beta: the firm's sensitivity to market returns, estimated over the 36 months before the call
- Momentum: the stock's return over the prior twelve months, skipping the most recent month

**Market adjustment:** Overall market returns are absorbed by the intercept i each monthly cross-section, and each firm's exposure to the market is controlled through its estimated beta.

**Inference:** The average estimated effect of the language measure across months, with Newey-West standard errors. Cross-sections are run by call month.

**Failure condition:** If the average effect of the language measure is statistically indistinguishable from zero once earnings surprise and the other controls are included, the language signal does not add information beyond the earnings numbers, and the hypothesis is rejected.

All tests beyond the primary specification are exploratory and will be reported as such.