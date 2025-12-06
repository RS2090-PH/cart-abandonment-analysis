# Problem Statement: Financial Impact of Cart Abandonment on MyCoke360 Revenue and Product Mix


## Business Problem

MyCoke360 is a digital ordering platform for B2B customers that launched in summer 2024. The platform serves FSOP customers and logs web events and item interactions. Cart abandonment is defined as a customer adding an item to a cart and not completing a purchase by the next expected order date based on the Swire’s ordering rules. The specific question for this workstream is: what is the financial impact of cart abandonment on total MyCoke360 revenue and on the composition of product sales by brand and pack type.


## Benefit of a Solution

Quantifying lost revenue and mix distortion will allow the business to size the opportunity, prioritize fixes, and target interventions where they matter most. Clear measurement of lost dollars, recovered dollars, and net revenue impact provides an objective basis for investment decisions. Understanding which brands and pack types are overrepresented in abandoned value versus realized sales will support pricing, merchandising, and inventory actions that protect revenue while improving the customer experience.


## Analytics Approach

This analysis integrates Google Analytics events with orders and sales to measure lost value and to attribute that value to product groups. Event timestamps in GA are recorded in EST and will be converted to each customer’s local time using the sales office or plant. Order windows are constructed from anchor date, frequency, and local cutoff time, with exceptions applied where specified. Abandonment is labeled when an item is added but no purchase occurs within that window, and the label is corrected when an order exists for that window in the orders table. Revenue per item is estimated from sales using NSI_DEAD_NET at the material and date level to value abandoned items because GA does not record price unless the item is purchased.


## Success Metrics

Success is defined by a focused set of financial and mix metrics that can be produced from the one-year data window. The baseline is total MyCoke360 revenue for the period. Lost revenue is the estimated dollar value of items in abandoned windows. Recovered revenue is the realized revenue for items that are purchased within the defined recovery window after an initial abandonment. Net revenue impact is lost revenue minus recovered revenue and is also expressed as a percent of total revenue. Mix impact is measured by comparing abandoned value share with sales value share by brand and pack type and by listing the top at-risk SKUs by lost dollars and by frequency of appearance in abandoned windows.


## Scope

This workstream will deliver a reconciled dataset and calculations required to compute the baseline revenue, lost revenue, recovered revenue, net impact, and mix comparisons by brand and pack type. It will also deliver a concise summary of top at-risk SKUs by lost dollars and frequency. Items outside scope include broader behavioral modeling, UI design, or cross-channel churn analyses, which are addressed by other project workstreams.


## Details

The analysis period is 5/31/2024 through 5/26/2025. Data sources include GA events for site interactions and associated items, orders for what was ordered, and sales for realized revenue using NSI_DEAD_NET. Dimension tables provide customer, visit plan history, operating hours, cutoff time exceptions, and material attributes such as brand, flavor, pack size, and pack type. Known limitations include missing GA purchase events, mismatches between GA cart or purchase items and the orders table, and blank item details for some mobile purchases. These limitations will be mitigated by reconciling GA with orders to correct abandonment labels and by valuing items using sales data.

**Key Deadlines:**

* 9/12/2025: **Draft Workstream Problem Statement** (Ali Ladha)
* 9/12/2025: **Draft Workstream Problem Statement** (Cyrus Sobhani)
* 9/12/2025: **Draft Workstream Problem Statement** (Robby Stohel)
* 9/12/2025: **Draft Workstream Problem Statement** (Sterling Leduc)
* 9/13/2025: **Compile Final Problem Statement** (Robby Stohel)
* 9/14/2025: **Submit Final Problem Statement** (Ali Ladha, Cyrus Sobhani, Sterling Leduc, Robby Stohel)
* 10/02/2025: **Draft Workstream EDA Notebook** (Ali Ladha)
* 10/02/2025: **Draft Workstream EDA Notebook** (Cyrus Sobhani)
* 10/02/2025: **Draft Workstream EDA Notebook** (Sterling Leduc)
* 10/02/2025: **Draft Workstream EDA Notebook** (Robby Stohel)
* 10/04/2025: **Compile Final EDA Notebook** (Robby Stohel)
* 10/05/2025: **Submit Final EDA Notebook** (Ali Ladha)
* 10/23/2025: **Draft Workstream Modeling Notebook** (Ali Ladha)
* 10/23/2025: **Draft Workstream Modeling Notebook** (Cyrus Sobhani)
* 10/23/2025: **Draft Workstream Modeling Notebook** (Sterling Leduc)
* 10/23/2025: **Draft Workstream Modeling Notebook** (Robby Stohel)
* 10/25/2025: **Compile Final Modeling Notebook** (Robby Stohel)
* 10/26/2025: **Submit Final Modeling Notebook** (Ali Ladha, Cyrus Sobhani, Robby Stohel, Sterling Leduc)
* 11/14/2025: **Develop Presentation Deck** (Sterling Leduc)
* 11/15/2025: **Prepare Practice Presentation** (Ali Ladha, Cyrus Sobhani, Robby Stohel)
* 11/16/2025: **Submit Practice Presentation Materials** (Ali Ladha)
* 12/07/2025: **Submit Group GitHub Portfolio** (Ali Ladha)
* 12/07/2025: **Submit Individual GitHub Portfolio** (Cyrus Sobhani)
* 12/07/2025: **Submit Individual GitHub Portfolio** (Robby Stohel)
* 12/07/2025: **Submit Individual GitHub Portfolio** (Sterling Leduc)
* 12/08/2025: **Deliver Final Presentation (On Campus)** (Ali Ladha, Cyrus Sobhani, Robby Stohel, Sterling Leduc)

