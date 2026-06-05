
# Blinkit Quick Commerce & Inventory Intelligence Dashboard

### Dashboard Link : https://app.powerbi.com/groups/me/reports/970509bb-98c2-4bec-ab2b-a9ec2e530e36/1af8888980cb3fdd4a46?experience=power-bi

## Situation (Problem Statement)

The quick-commerce (Q-commerce) industry operates on extremely tight margins and hyper-accelerated timelines, promising deliveries in under 10 to 15 minutes. For companies like Blinkit ("India's Last Minute App"), this requires an absolutely flawless micro-fulfillment strategy across a network of "dark stores" and retail partnerships. 

Managing a sprawling catalog of Fast-Moving Consumer Goods (FMCG)—ranging from highly perishable fruits to household staples—presents a massive logistical challenge. Regional directors and supply chain managers often lack a centralized, unified view of their localized operations. They struggle to answer complex multidimensional questions:
*   *Which store formats (Grocery vs. Supermarket Types) are yielding the highest ROI?*
*   *How does consumer demand for healthy (Low Fat) versus traditional (Regular) products shift depending on the geographic tier (Tier 1 vs. Tier 3)?*
*   *Is prime shelf space (Item Visibility) effectively correlating with total sales volume?*

Without a highly interactive, data-dense business intelligence dashboard, decision-makers are forced to rely on fragmented ERP reports. This leads to inefficient capital allocation, inventory stockouts of trending categories (like snacks and fresh produce), and an inability to optimize the physical footprint of their retail outlets.

## Task

The core objective was to engineer a comprehensive, single-pane-of-glass Power BI dashboard that serves as a **Retail & Inventory Command Center**. The specific technical and analytical goals included:
1.  **Unified Metric Tracking:** Develop dynamic KPIs for Total Sales, Average Order Value/Sales, Inventory Depth (No. of Items), and Customer Satisfaction (Avg Rating).
2.  **Granular Product Slicing:** Map out revenue generation across 15+ distinct product categories and dissect dietary purchasing trends.
3.  **Spatial & Structural Analysis:** Evaluate store performance across intersecting dimensions: Geographic Location (Tiers 1, 2, 3), Physical Size (Small, Medium, High), and Outlet Type.
4.  **Historical Diagnostics:** Track aggregate revenue against the historical establishment timeline of the outlets to determine if older stores outperform newer expansions.
5.  **Interactive UI/UX:** Create a highly navigational interface using interactive bookmark buttons and slicers, strictly adhering to Blinkit’s brand guidelines (high-contrast yellow and green).

## Action (Steps Followed)

The dashboard development was executed through a rigorous end-to-end data modeling and visual engineering workflow:

- **Step 1 : Data Extraction & Normalization:** Ingested the raw retail dataset into Power Query. Handled missing values, standardized product category nomenclatures, and validated numeric fields to ensure accurate aggregation of sales and visibility metrics.
- **Step 2 : UI/UX & Brand Theming:** Applied a custom canvas background utilizing Blinkit’s signature yellow for the primary left-hand navigation pane and title block. Designed custom floating card containers with soft drop-shadows to separate key analytical zones.
- **Step 3 : Dynamic KPI Banner Integration:** Programmed DAX measures to calculate and display top-level metrics: **Total Sales ($1.20M)**, **Avg Sales ($141)**, **No of Items (8523)**, and **Avg Rating (3.9)**, incorporating relevant iconography for immediate visual recognition.
- **Step 4 : Interactive Navigation Build:** 
    *   Constructed a primary slicer panel on the left (Outlet Location Type, Outlet Size, Item Type) allowing users to filter the entire report globally.
    *   Engineered a toggle menu (Total Sales, Avg Sales, No of Items, Avg Rating) above the charts to allow users to dynamically change the underlying measure of the visuals.
- **Step 5 : Consumer Behavior & Product Mapping:**
    *   Built a Donut Chart (**"Fat Content"**) and a localized Stacked Bar Chart (**"Fat by Outlet"**) to analyze the dietary split.
    *   Deployed a dense Horizontal Clustered Bar Chart (**"Item Type"**) to rank inventory categories, sorting them descending by total sales volume.
- **Step 6 : Geographical & Capacity Modeling:**
    *   Developed an **"Outlet Size"** Donut Chart to map revenue distribution among High, Medium, and Small capacity footprints.
    *   Engineered a modified Funnel/Bar Chart for **"Outlet Location"** to explicitly rank sales across Tier 1, Tier 2, and Tier 3 markets.
- **Step 7 : Historical & Format Matrix Engineering:**
    *   Plotted an **"Outlet Establishment"** time-series area chart spanning a decade (2012-2022) to map the lifecycle curve of store revenue.
    *   Constructed an advanced **"Outlet Type"** data matrix equipped with conditional formatting (data bars/color scales) to cross-evaluate sales, inventory count, average rating, and item visibility ratios by specific store formatting.

## Result (Deep Insights & Data Inferences)

The resulting dashboard acts as a highly effective analytical tool. Based on the snapshot of the current aggregate data state, profound business inferences can be drawn:

### [1] Macro Financials & Inventory Health

![image alt](https://github.com/user-attachments/assets/9da8243f-18bc-4a76-8404-edb6f245061f)

*   The dashboard encompasses a robust global footprint, processing **8,523 distinct inventory items** that drive **$1.20 Million** in total revenue.
*   Despite the high volume of rapid transactions typical of Q-commerce, the **Average Sales** value maintains a strong **$141** baseline, supported by an impressive overall customer satisfaction rating of **3.9 out of 5**.

### [2] The Dominance of "Healthy" Quick Commerce

![image alt](https://github.com/user-attachments/assets/d34862fb-6eda-4606-adb6-83a8b686f60d)

*   **Dietary Shift:** Consumers overwhelmingly prioritize healthier options even in "last-minute" purchases. **Low Fat** products represent the vast majority of sales (**$776.32K**), nearly doubling the revenue generated by Regular fat content items (**$425.36K**).
*   **Regional Dietary Consistency:** The Stacked Bar chart reveals this trend is uniform across all geographic areas. Whether in Tier 1 or Tier 3 locations, Low Fat items consistently outpace Regular items by a wide margin.

### [3] Category Performance Rankings

![image alt](https://github.com/user-attachments/assets/56806b2e-6a6f-4de8-8a16-a2f3da96fa3f)

*   **Top Tier Revenue Drivers:** Perishables and impulse buys rule the platform. **Fruits and Vegetables** tied exactly with **Snack Foods** for the number one spot, each generating **$0.18M**. **Household** goods follow closely at **$0.14M**.
*   **Mid-to-Low Performers:** Essential but slower-moving categories like **Baking Goods ($0.08M)**, **Meat ($0.06M)**, and **Breads ($0.04M)** sit in the middle.
*   **Niche Markets:** At the very bottom of the spectrum, **Breakfast ($0.02M)** and **Seafood ($0.01M)** generate minimal revenue, suggesting these might not be optimal categories for premium dark-store shelf space.

### [4] Geographic Footprint & Sizing Strategy

![image alt](https://github.com/user-attachments/assets/f80ec506-042b-40a9-8b4f-f79c951ad07f)

*   **The Tier 3 Anomaly:** Contrary to assumptions that Tier 1 metros drive maximum revenue, **Tier 3 locations are the primary economic engine**, generating a massive **$472.13K**. Tier 2 follows with **$393.15K**, leaving Tier 1 at the bottom with **$336.40K**. This indicates massive quick-commerce penetration in developing/suburban markets.
*   **The "Medium" Sweet Spot:** Over-indexing on massive warehouse spaces is inefficient. **Medium-sized outlets** generated the most capital at **$507.90K**, easily outpacing Small (**$444.79K**) and significantly outperforming High-capacity stores (**$248.99K**).

### [5] Format Typology & Item Visibility

![image alt](https://github.com/user-attachments/assets/d907375d-c445-4473-bb2e-ba8a101ca098)

*   **Flagship Format:** **Supermarket Type 1** is the undisputed backbone of the operation, hauling in a staggering **$787.55K** in total sales and housing the bulk of the inventory (**5,577 items**).
*   **The Visibility Paradox:** Basic **Grocery Stores** hold the highest **Item Visibility score (0.10)** across all formats, yet they only account for **$151.94K** in sales. Conversely, the massive Supermarket Type 1 has a lower visibility score (0.06) but moves exponentially more product. This suggests that in dark-store operations, raw catalog volume and variety trump specific item placement visibility.

### [6] Historical Lifecycle Curve

![image alt](https://github.com/user-attachments/assets/ef02049e-e0fb-4af3-8a4f-00d214eca59c)

*   **The 2018 Boom:** The *Outlet Establishment* area chart shows a clear expansion lifecycle. Stores established early (2012) plateaued around **$130K**. However, stores opened during the **2018 expansion wave** are currently the highest-yielding assets, peaking at **$205K**.
*   **Post-2018 Correction:** After the 2018 peak, revenue for newer establishments sharply corrected, stabilizing back into the **$129K - $131K** range for stores opened between 2020 and 2022.

## Future Enhancements

To further advance the strategic value of this reporting ecosystem, subsequent iterations will focus on:
*   **Time-Intelligence Analytics:** Adding Year-to-Date (YTD) and Month-over-Month (MoM) growth calculations to track the velocity of sales in real-time.
*   **Predictive Stockout Modeling:** Utilizing machine learning extensions to forecast inventory depletion rates for top-tier categories (Snacks and Fruits/Veg) to automate reordering protocols.
*   **Profitability vs. Revenue:** Integrating Cost of Goods Sold (COGS) and delivery operational costs to shift the dashboard's focus from top-line Total Sales to bottom-line Net Profit margin analysis.

## How to Interact

*   **Dynamic Canvas Toggles:** Use the grey and yellow buttons above the Fat Content chart (Total Sales, Avg Sales, No of Items, Avg Rating) to instantly shift the visual perspective of the entire dashboard to a new metric.
*   **Cross-Filtering:** Click directly on any visual element—such as the "Tier 3" bar on the Location chart or the "Low Fat" section of the Donut chart—to cross-filter all other visuals and analyze highly specific micro-segments of the data.



