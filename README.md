### Data Scientist | Experimentation, ML & AI | Software Engineering background

> *I help companies make better decisions with data — and I can build the systems that make those decisions reliable.*

My work starts from a business question and ends in a decision: a ship / don't-ship memo, a metric a team can steer by, a model tied to a business cost. The engineering side is how I make that work reproducible.

**How I work**

- **Decide the rule before opening the data.** Hypothesis, primary metric and ship threshold are written down first.
- **Every finding carries its limitations.** If a number can't support a decision, the report says so.
- **Audit my own definitions.** In the Olist project I found and corrected two of my own metric errors, and documented how large each one was.

---

## Portfolio

Each project lives in its own repository and follows the same structure: **Problem → Data → Method → Key Findings → How to run**. The projects are built in order, and each level adds one new set of tools.

### Level 0 — Foundations

<table>
<tr>
<td width="45%" valign="top">
<a href="https://github.com/veysellball/olist-ecommerce-sql-eda"><img src="https://raw.githubusercontent.com/veysellball/olist-ecommerce-sql-eda/main/reports/05_delivery_satisfaction.png" alt="Delivery time vs. customer satisfaction"></a>
</td>
<td valign="top">
<b><a href="https://github.com/veysellball/olist-ecommerce-sql-eda">Olist E-Commerce — SQL &amp; EDA</a></b>
<br><br>
Five business decisions from 96,478 Brazilian marketplace orders. Late deliveries score <b>2.02 points lower</b> (2.27 vs. 4.29 out of 5), and 29% of misses are only 1–3 days late: padding the delivery estimate fixes them without touching logistics.
<br><br>
<code>SQL</code> <code>DuckDB</code> <code>pandas</code> <code>Matplotlib</code>
<br><br>
<a href="https://github.com/veysellball/olist-ecommerce-sql-eda/blob/main/notebooks/04_findings.ipynb">Findings report →</a>
</td>
</tr>
</table>

### Level 1 — Statistics, Experiments & Causality

<table>
<tr>
<td width="45%" valign="top">
<a href="https://github.com/veysellball/cookie-cats-ab-test"><img src="https://raw.githubusercontent.com/veysellball/cookie-cats-ab-test/main/reports/04_effect_summary.png" alt="A/B test effect with 95% confidence interval"></a>
</td>
<td valign="top">
<b><a href="https://github.com/veysellball/cookie-cats-ab-test">Cookie Cats — A/B Test</a></b>
<br><br>
Should a mobile game move its first progress gate from level 30 to 40? Across 90,189 players the answer is <b>don't ship</b>: 7-day retention falls 0.82 points (95% CI [−1.33, −0.31]). Includes a power analysis, SRM and A/A checks, and a peeking simulation (5.1% → 16.3% false positives).
<br><br>
<code>SciPy</code> <code>statsmodels</code> <code>bootstrap</code> <code>power analysis</code>
<br><br>
<a href="https://github.com/veysellball/cookie-cats-ab-test/blob/main/reports/decision_memo.md">Decision memo →</a>
</td>
</tr>
</table>

🔄 **In progress — Business Metrics & Dashboard:** a metric framework for Olist that defends a north star metric (and argues why retention isn't it), plus a live Streamlit dashboard.

**Next:** causal inference (DoWhy) → churn classification with MLflow + CI → demand forecasting with uncertainty → an evaluated LLM analyst (text-to-SQL + RAG) → deployment with FastAPI and Docker.

---

## Other projects

Earlier work outside the data science series:

- **[Stress & Fatigue Detector](https://github.com/veysellball/Human-Computer-Interaction-Stress-Fatigue-Detector)**: collects keyboard, mouse and active-window telemetry in real time and uses machine learning to detect stress and fatigue.
- **[BlogIntern](https://github.com/veysellball/BlogIntern)**: .NET Core backend.

---

## Toolkit

**Used in published projects:** Python · SQL (DuckDB) · pandas · NumPy · SciPy · statsmodels · Matplotlib · Jupyter · Git

<!-- TODO: add contact links (LinkedIn, email) -->
