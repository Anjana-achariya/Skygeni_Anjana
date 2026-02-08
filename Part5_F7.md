**What assumptions in your solution are weakest?**

Sales behavior, market demand, pricing, or competition can change quickly, and the rules built from past data may become less accurate over time.

Another weak assumption is that all long sales cycles are bad, even though some large or complex deals naturally take longer.

**What would break in real-world production?**

The system would struggle if the input data quality drops, such as missing updates, incorrect deal stages, or delayed closures in the CRM.

New regions, lead sources, or products with little historical data would also reduce the reliability of risk signals. 

Sudden market changes or seasonality could cause the rules to generate false alerts.

**What would you build next if given 1 month?**

I would add a lightweight predictive model alongside the rules to estimate deal-loss probability and compare it with the rule-based score.

Also would add UI or dashboard and will use Airflow to run it scheduled .

I would build a small feedback loop where sales managers can confirm or dismiss alerts to improve the system.

**What part of your solution are you least confident about?**

I am least confident about the fixed thresholds used in the rules, such as the average sales cycle used to define long-running deals.
