# Megaline-Telecom-Plan-Study
In this statistical data analysis project for telecom operator Megaline, we will determinie which prepaid plans, Surf and Ultimate, brings in more revenue in order to determine their budget for their advertising team.

I will analyze the clients' behavior by using data from 500 Megaline customers. The data includes which plan the clients use, where they are from, who the clients are, the number of calls made, and the text messages sent from 2018. Based on this data, I will then conclude which prepaid plan brings in more revenue by using hypothesis.

- Null Hypothesis: No difference in average revenue between Ultimate and Surf Plans
- Alt. Hypothesis: Difference in average revenue between Ultimate and Surf Plans

# Description 
The `users` table (data on users):

- user_id — unique user identifier
- first_name — user's name
- last_name — user's last name
- age — user's age (years)
- reg_date — subscription date (dd, mm, yy)
- churn_date — the date the user stopped using the service (if the value is missing, the calling plan was being used when this database was extracted)
- city — user's city of residence
- plan — calling plan name

The `calls` table (data on calls):

- id — unique call identifier
- call_date — call date
- duration — call duration (in minutes)
- user_id — the identifier of the user making the call

The `messages` table (data on texts):

- id — unique text message identifier
- message_date — text message date
- user_id — the identifier of the user sending the text

The `internet` table (data on web sessions):

- id — unique session identifier
- mb_used — the volume of data spent during the session (in megabytes)
- session_date — web session date
- user_id — user identifier

The `plans` table (data on the plans):

- plan_name — calling plan name
- usd_monthly_fee — monthly charge in US dollars
- minutes_included — monthly minute allowance
- messages_included — monthly text allowance
- mb_per_month_included — data volume allowance (in megabytes)
- usd_per_minute — price per minute after exceeding the package limits (e.g., if the package includes 100 minutes, the 101st minute will be charged)
- usd_per_message — price per text after exceeding the package limits
- usd_per_gb — price per extra gigabyte of data after exceeding the package limits (1 GB = 1024 megabytes)



# Conclusion
- Distinct Usage Patterns and Revenue across Plans: Analysis revealed statistically significant differences in average revenue between the "Ultimate" and “Surf” plans. This indicates that the choice of plan materially impacts user behavior in terms of usage and, consequently, the revenue generated for the telecom provider.

- Assumption: We assumed that the difference in plan features directly affected user choice and usage behavior. Our analysis did not account for external factors such as user demographics or regional network quality, which could also influence usage patterns.

- Geographical Influence on Revenue: By comparing users in the NY-NJ area to those in other regions, the test aimed to identify if the geographical location influenced revenue generation. While specific outcomes depended on the analysis results, the attempt to segment revenue based on location underscores an assumption that regional market dynamics might affect usage and revenue.

- Assumption: The geographic segmentation presumed that the only significant regional difference was location itself, rather than associated factors like regional marketing efforts or local competition.

Methodological Decisions:

- The decision to use a two-sample t-test (specifically, Welch’s t-test for cases of unequal variance) was driven by an intention to compare means between two independent groups. This choice hinged on assumptions of normal distribution patterns of revenue within groups and the adequacy of sample sizes. Setting an alpha value of 0.05 was a balance between avoiding Type I errors (falsely detecting an effect) and Type II errors (failing to detect a real effect), considered standard practice in many analyses.

Data Quality and Integration:

- Successful merging of user data with usage logs required a clean, shared identifier (user_id).

Assumption: There was an underlying assumption that the recorded user_id matches across different datasets were accurate and that there was a 1:1 relationship where necessary for merging.

- Implications for Telecom Provider:

The differences in revenue across plans and potential geographical variations offer actionable insights for targeted marketing, plan optimization, and regional strategy development. Identifying high-revenue user segments enables more efficient allocation of marketing resources.

- Decision: The analysis implicitly suggested focusing on segments with higher average revenue or usage could maximize ROI for the telecom provider.

Future Analysis Recommendations:

- Further investigation into the causes behind the differences in usage and revenue generation, including demographic analysis, user satisfaction surveys, and more detailed regional market analysis, could provide deeper insights. Exploration of seasonal trends, promotional impacts, and longitudinal studies on user behavior change over time with plan upgrades or downgrades could enrich understanding.

These conclusions and the processes leading up to them highlight the importance of data-driven decision-making in strategic business planning, while also underscoring the relevance of critical assumptions in shaping analysis outcomes.
