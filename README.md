# Earnings-call-signals

Do earnings call transcripts predict stock returns beyond what the earnings surprise already tells us?

**Status:** In progress. Data collection and pipeline setup.

## Research Question

Does negative or uncertain language in management's Q&A answers on earnings calls predict subsequent stock returns, beyond what earnings surprise and known return predictors already explain?

## Hypothesis

Firms whose management uses more negative and uncertain language in Q&A answers earn lower returns over the month following the call. The hypothesis is pre-registered in [docs/hypotheses.md (docs/hypotheses.md), including the primary specification and what would count as failure.

## Data

| Data | Source | Coverage |
|---|---|---|
| Earnings call transcripts | [source, to be confirmed] | [number of calls, date range] |
| Prices, earnings, analyst consensus, fundamentals | Bloomberg | [universe, date range] |
| Fama-French factor returns | Ken French Data Library | [date range] |


## Method

1. Parse transcripts into prepared remarks and Q&A, and separate management from analysts
2. Measure negative and uncertain language in management's Q&A answers using the Loughran-McDonald financial dictionary
3. Compute post-call returns and earnings surprise relative to analyst consensus
4. Test the relationship with Fama-MacBeth cross-sectional regressions, controlling for earnings surprise, announcement reaction, firm size, book-to-market, market beta, and momentum
5. Extend with portfolio sorts, FinBERT and embedding-based features, and machine learning models, each compared against simpler baselines using time-based validation

## Evaluation Principles

- Results are judged by whether language adds information beyond earnings surprise and known return predictors
- Models are validated only on later time periods than they were trained on
- Standard errors account for clustering of calls in time and across firms
- Failed approaches and null results are reported alongside successes

## Results

[To be completed. Include the headline finding, one key table, and one figure. Report null or negative results here too.]

## Limitations

[To be completed. Cover sample and data gaps, timing assumptions, risk of lookahead bias, and what could not be tested.]

## Repository Layout

- `docs/`: pre-registered hypotheses, data notes, and final write-up
- `src/`: code for data loading, features, outcomes, analysis, and models
- `notebooks/`: exploratory analysis
- `tests/`: checks for timing and lookahead bias
- `results/`: figures and tables (aggregate outputs only)
- `config.yaml`: universe, date range, and window settings

## Reproducing the Analysis

[To be completed once the pipeline is built. Describe environment setup, the order in which to run each step, and how to supply your own Bloomberg and transcript data.]

## References

[Add the 3 to 5 academic papers this project builds on.]