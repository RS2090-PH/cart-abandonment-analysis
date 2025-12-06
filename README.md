# Cart Abandonment Revenue Impact Analysis - MSBA Capstone Project
 
This repository presents the analytical work performed as part of the Master of Science in Business Analytics (MSBA) Capstone Project in partnership with Swire Coca-Cola, USA. The project evaluates the financial and product-mix implications of cart abandonment on the MyCoke360 digital ordering platform. The analysis adheres to established analytical methodology and supports stakeholders with measurable, defensible insights using production-grade data.


### Methodology

This project follows the CRISP-DM methodology used across the analytics portfolio:

1. Business Understanding - Clarifying the revenue, customer-behavior, and product-mix questions posed by Swire stakeholders and defining measurable outcomes.
2. Data Understanding - Reviewing eight structured tables (events, orders, sales, and supporting dimensions) to map system behaviors, temporal rules, and product attributes.
3. Data Preparation - Reconciling timestamps, constructing order windows, correcting abandonment labels, integrating GA events with order and sales systems, and building an analysis-ready dataset.
4. Modeling / Measurement - Implementing the rule-based abandonment logic, valuing abandoned items with sales pricing, and computing revenue and mix impacts.
5. Evaluation - Validating calculations against business definitions, testing edge cases around frequency rules and cutoff times, and confirming metric consistency.
6. Deployment - Delivering reproducible notebooks, documented logic, and metrics ready for stakeholder review and downstream decision-making.


### Data Source

The project uses eight CSV tables capturing customer behavior, transactions, scheduling rules, and product definitions. These tables provide a complete operational view enabling revenue, behavior, and product-mix analysis.

Three fact tables describe activity on MyCoke360:

- Google Analytics Events - Site interactions including visits, add/remove cart actions, device and page metadata, and purchase events.
- Orders - All materials ordered, with timestamps in EST and UTC, order types, and customer-specific details.
- Sales - Fulfilled transactions with revenue and profit metrics (including NSI_DEAD_NET for valuation).

Five dimension tables provide structure:

- Customer - Account attributes, channels, and associated sales offices.
- Cutoff Times - Delivery and ordering policies by plant, office, and distribution mode.
- Material - Product master data including brand, flavor, pack type, and category.
- Operating Hours - Customer-specific frequencies and anchor days/dates.
- Visit Plan - Historical anchor dates, ordering patterns, and sales office attributes.


### Business Problem

MyCoke360 allows FSOP customers to place digital orders; however, many customers add items to their carts but do not complete their purchases before their next expected ordering window. The key questions are to quantify:

- The financial impact - of these abandoned items on total revenue,
- The extent of recovered revenue - when customers later purchase previously abandoned items, and
- The product-mix distortion - created when certain brands or pack types appear disproportionately in abandoned carts.


### Potential Solution

The proposed solution integrates event-level behavior with transaction-level outcomes to reconcile abandonment patterns, estimate lost dollars, and assess recovery. Using order-window logic based on anchor dates, customer frequencies, and cutoff times, each cart action is evaluated to determine whether an item was purchased in the expected window or left abandoned. Valuation relies on sales data rather than GA metadata, ensuring pricing accuracy. This framework produces defensible financial metrics and mix comparisons.


### Business Value

A clear measurement of lost and recovered revenue helps Swire size the commercial impact of abandonment and identify high-value opportunities:

- Revenue Opportunity Sizing - Establishing the dollar value at risk due to abandonment and the portion recoverable under improved experiences.
- Targeted Interventions - Highlighting specific brands, pack types, and SKUs that contribute disproportionately to lost value.
- Improved Merchandising & Pricing Decisions - Using mix distortion metrics to adjust presentation, pricing, or promotion strategies.
- Operational Efficiency - A standardized, reproducible process enables ongoing monitoring across future data periods.

These outputs support data-driven investment and prioritization decisions.


### Personal Contribution

I directly managed the code repository, development workflow, and integration process for the workstream. My responsibilities included:

- Maintaining and organizing all notebooks, including planning, compilation, formatting, documentation, and conversion work (pandas to PySpark where needed).
- Leading the consolidation of all teammates’ analyses into a unified, production-quality notebook.
- Designing and building custom helper functions to standardize repeated logic.
- Coordinating with team members to ensure their deliverables aligned with the repository structure and compilation requirements.
- Owning one of the business questions while also creating dedicated EDA and modeling notebooks (ongoing), portions of which contributed directly to the compiled workstream output.

This dual role ensured both analytical contribution and technical stewardship of the project.


### Project Difficulties

Several challenges emerged:

- Coordination and timeline alignment across teammates, particularly with varying availability.
- Differences in analytical expectations, such as whether EDA should be general or tailored to the business questions.
- Mixed technical experience with pandas and PySpark, requiring mediation and standardization.
- Shifts in direction mid-process, necessitating adjustments to notebook structure and development pace.

These constraints required active communication, planning, and technical adaptation.


### Learning Outcomes

This project strengthened multiple competencies:

- Enhanced communication and cross-team collaboration.
- Deeper experience working with large, operational datasets from a real business system.
- Improved proficiency with Python-based analytics, PySpark workflows, and Databricks.
- Continued application of the CRISP-DM framework to structure analytical reasoning.
- Additional exposure to production-grade data pipelines, timing rules, and business logic interpretation.

These experiences contribute directly to professional readiness for applied analytics roles.


### Acknowledgments

This project is a part of the coursework for the Master of Science in Business Analytics (MSBA) program at the University of Utah. We extend our gratitude to the University of Utah for providing the academic foundation and resources to pursue this analysis. Additionally, we thank Swire for providing the dataset, business problems and enabling the competition.

