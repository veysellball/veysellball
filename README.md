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

<table>
<tr>
<td width="45%" valign="top">
<a href="https://github.com/veysellball/causal-inference"><img src="https://raw.githubusercontent.com/veysellball/causal-inference/main/reports/dag.png" alt="Causal DAG: delivery delay and review score"></a>
</td>
<td valign="top">
<b><a href="https://github.com/veysellball/causal-inference">Olist — Causal Inference: Delivery Delays &amp; Review Sentiment</a></b>
<br><br>
Late orders get 56.6 points fewer 4–5★ reviews, but is lateness the cause? On 93,832 orders, adjusting for 44 confounders shows the true penalty is about <b>−34 points (ATT)</b>: roughly 40% of the naive gap is selection bias. Includes a causal DAG, backdoor identification, propensity matching, IPW and doubly robust estimation, with balance and overlap diagnostics.
<br><br>
<code>DoWhy</code> <code>statsmodels</code> <code>propensity scores</code> <code>DAG</code>
<br><br>
<a href="https://github.com/veysellball/causal-inference#key-findings">Key findings →</a>
</td>
</tr>
</table>

### Level 2 — Business Metrics & BI

<table>
<tr>
<td width="45%" valign="top">
<a href="https://github.com/veysellball/business-metrics-dashboard"><img src="https://raw.githubusercontent.com/veysellball/business-metrics-dashboard/main/ScreenShots/mainPage.png" alt="Olist business health dashboard"></a>
</td>
<td valign="top">
<b><a href="https://github.com/veysellball/business-metrics-dashboard">Olist Business Health — Metric Framework &amp; Live Dashboard</a></b>
<br><br>
Which single number should a marketplace steer by? The north star is <b>Good Orders</b> (on time + 4–5★ review): only 74.4% of orders become one, and the biggest loss comes after delivery. Retention is rejected as the north star: only 1.99% of buyers return within 180 days, and doubling that adds just ≈2.2% to GMV.
<br><br>
<code>DuckDB</code> <code>pandas</code> <code>Streamlit</code> <code>metric design</code>
<br><br>
<a href="https://business-metrics-dashboard-wxi8bdappzgugs8nuetupfx.streamlit.app">Live dashboard →</a> · <a href="https://github.com/veysellball/business-metrics-dashboard/blob/main/reports/metric_dictionary.md">Metric dictionary →</a>
</td>
</tr>
</table>

<table>
<tr>
<td width="45%" valign="top">
<a href="https://github.com/veysellball/olist-ecommerce-powerbi-dashboard"><img src="https://raw.githubusercontent.com/veysellball/olist-ecommerce-powerbi-dashboard/main/ScreenShots/health_overview.png" alt="Power BI Health Overview page"></a>
</td>
<td valign="top">
<b><a href="https://github.com/veysellball/olist-ecommerce-powerbi-dashboard">Olist Business Health — Power BI Metric Layer</a></b>
<br><br>
The same Good Orders metric framework rebuilt as a Power BI semantic model (star schema, 2 fact tables, DAX measures, 6 report pages). A dedicated reconciliation page proves every metric matches the Python model: <b>99,092 orders, 73,734 Good Orders and GMV to the cent, with zero difference in every month</b>. Includes a Power BI vs. Streamlit comparison on when to use which.
<br><br>
<code>Power BI</code> <code>DAX</code> <code>Power Query</code> <code>TMDL / PBIP</code> <code>reconciliation</code>
<br><br>
<a href="https://github.com/veysellball/olist-ecommerce-powerbi-dashboard/blob/main/docs/dax_measures.md">DAX catalog →</a> · <a href="https://github.com/veysellball/olist-ecommerce-powerbi-dashboard/blob/main/docs/metric_dictionary.csv">Metric dictionary →</a>
</td>
</tr>
</table>

### Level 3 — Forecasting at Scale *(in progress)*

<table>
<tr>
<td valign="top">
<b><a href="https://github.com/veysellball/m5-forecasting-spark">M5 Forecasting at Scale — PySpark &amp; LightGBM</a></b> 🚧
<br><br>
How much will each Walmart store sell over the next 28 days, and how sure are we? Forecasting all 30,490 item-store series of M5 (≈59M rows): a leakage-free feature pipeline in PySpark on Databricks, per-series baselines trained in parallel with <code>applyInPandas</code>, and LightGBM evaluated with rolling-origin backtests and P10/P90 intervals for store replenishment. The validation plan is committed before any model is trained, and a pytest suite in CI checks that no feature can see the future.
<br><br>
<code>PySpark</code> <code>Databricks</code> <code>LightGBM</code> <code>MLflow</code> <code>pytest</code> <code>GitHub Actions</code>
<br><br>
<a href="https://github.com/veysellball/m5-forecasting-spark">Repository →</a>
</td>
</tr>
</table>

**Next:** an evaluated LLM analyst (text-to-SQL + RAG) → deployment with FastAPI, Docker and Airflow.

---

## Other projects

Earlier work outside the data science series:

- **[Stress & Fatigue Detector](https://github.com/veysellball/Human-Computer-Interaction-Stress-Fatigue-Detector)**: collects keyboard, mouse and active-window telemetry in real time and uses machine learning to detect stress and fatigue.
- **[BlogIntern](https://github.com/veysellball/BlogIntern)**: .NET Core backend.

---

## Toolkit

**Used in published projects:** Python · SQL (DuckDB) · pandas · NumPy · SciPy · statsmodels · DoWhy · Matplotlib · Streamlit · Power BI (DAX, Power Query, star schema, PBIP/TMDL) · Jupyter · Git

<!-- TODO: add contact links (LinkedIn, email) -->
