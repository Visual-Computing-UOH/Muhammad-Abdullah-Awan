# Week 4 Progress Report — Muhammad Abdullah Awan

**Internship:** FlyRank AI — Machine Learning Engineering Track
**Lane:** Refresh / Content Opportunity Scoring
**Assignment:** w04_baseline_score.ipynb — Building the Rule-Based Baseline

## What I did this week

This week's task was to build a transparent, rule-based baseline that any
future machine learning model must beat — before doing any modeling myself.

### 1. Signal verification
I checked two real signals behind FlyRank's actual flagging logic:
- **Staleness vs. decline rate**: bucketed pages by days since last update
  and measured decline rate per bucket, with sample size (n) shown for
  each bucket. Compared against the overall base rate to reach a verdict.
- **Search position vs. CTR**: bucketed pages by average search position
  and measured average CTR per bucket, to confirm whether better position
  genuinely means higher click-through rate.

Each signal check ended with a one-word verdict (CONFIRMED / MIXED /
OPPOSITE) based on real data, not assumption.

### 2. Baseline rule
I encoded one transparent, hand-written rule:
- **Logic:** A page is flagged if it hasn't been updated in 180+ days
  AND still receives 500+ impressions (stale but visible).
- **Output:** A readable score, a reason code (`stale_but_visible`), and
  an action label (`review_for_refresh` or `monitor`).
- The full ranked queue was generated directly from the notebook and
  saved to `work/outputs/baseline_action_score.csv`.

### 3. Evaluation
- Measured **Precision@50** for the baseline rule and compared it against
  the base rate (random-guessing performance), to make the score
  meaningful rather than just a number.
- Saved metrics to `work/outputs/baseline_metrics.json`.

### 4. Top-10 manual review
Reviewed the top 10 flagged pages by hand. For each one, I documented:
- The action recommended
- Why it was flagged (the reasoning behind the score)
- What would make that specific flag wrong (e.g. seasonal traffic dips,
  or a related page absorbing the lost traffic instead of a genuine decline)

## Key takeaway
This baseline is intentionally simple and fully explainable — it is the
honest number that next week's machine learning model must beat. Locking
in this baseline before modeling ensures any future performance gain is
real, not just a moving target.

## Deliverable
Repo: https://github.com/abdullahawan0043-glitch/Flyrank-machine-learning-internship
Notebook: `work/notebooks/w04_baseline_score.ipynb`
