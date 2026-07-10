## Project Summary

A niche horror-only streaming competitor launches into the market. Primeflix wants to know: did this hurt us, and if so, who did it hurt?

Customers are split by genre-viewing behavior — Horror viewers (70%+ of watch time in horror) are the treated group, and Thriller viewers (70%+ of watch time in thriller) are the control group. Thriller viewers were chosen as the control because they show similar pre-launch engagement patterns to horror viewers but aren't served by a horror-only competitor, making them a credible counterfactual. This project uses Difference-in-Differences to estimate the causal impact of the competitor's launch on horror-viewer churn.

**Campaign Timeline**

| Period | Phase |
|---|---|
| Months 1-12 | Pre Launch Baseline behavior |
| Month 13 | Competitor Launch |
| Months 13-18 | Post Launch Measurement |

**Analysis Priorities**

1. **Parallel trends validation** - do Horror and Thriller viewers show statistically similar churn trends before the competitor launches? This is the credibility check that has to pass before any causal claim is made.
2. **Causal impact estimate** - using DiD, how much incremental churn did the competitor launch cause among Horror viewers, relative to Thriller viewers over the same period?
3. **Robustness checks** - does the effect hold up when the treatment/control threshold is redefined at 50%, 60%, and 70% horror/thriller viewing share, rather than relying on one arbitrary cutoff?

The genre segmentation is central to this analysis because a company can't just compare "affected" and "unaffected" customers without a pre-existing relationship between them - bundling all non-horror viewers together would violate the parallel trends assumption and produce an estimate that isn't defensible. I don't mind if the data is a little unrealistic; the focus is on demonstrating a rigorous causal inference workflow (problem framing, control group justification, pre-trend validation, estimation, and robustness) over data realism.

## Key Findings


## Recommendation




## Data Design Decisions
    ### Population

-   Total Primeflix subscriber base (implied): ~1,000,000
-   Horror viewers (treated group, 70%+ horror watch share): 80,000
-   Thriller viewers (control group, 70%+ thriller watch share): 100,000
-   Rationale: Horror and Thriller are treated as niche-concentration segments within a much larger, genre-mixed base — most subscribers don't concentrate 70%+ in a single genre. Thriller is sized larger than Horror to reflect its more mainstream appeal.

### Baseline churn rate

-   ~3–4% monthly churn, converted to weekly probability (Acquisition can be assumed to offset baseline churn at the topline business level)

## Timeline

78-week panel (18 months)
-   Weeks 1–52: pre-launch baseline
-   Week 53: competitor launches
-   Weeks 53–78: post-launch measurement window