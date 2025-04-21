# Bank_Loan_Analysis_Dashboard
An interactive dashboard for analyzing bank loan data to uncover approval trends, risk factors, and customer insights.

## Contents

- Project Overview
- Tools
- Data Overview
- Dashboard Structure
- Results

## Project Overview

The objective of this project was to design an interactive Tableau dashboard to visualize and analyze the performance of a bank’s loan portfolio. The dashboard provides stakeholders with insights into loan disbursements, repayment performance, credit risk indicators, and profitability metrics across various client profiles, loan types, and U.S. states.
The idea for this project emerged from a growing need in the banking industry to gain deeper insights into the performance of their loan portfolios. With loans being a critical source of revenue and risk for banks, the ability to monitor, analyze, and optimize lending decisions is essential for financial sustainability. Recognizing this, the project was conceptualized to leverage data visualization through Tableau to turn complex loan performance data into actionable insights.
This project was undertaken to explore the intersection of financial analytics and data visualization, with a focus on deriving insights from bank loan performance data. The objective was to convert raw data into an interactive dashboard capable of answering critical business questions that are often overlooked in traditional static reporting formats. Additionally, the project aligns with current industry trends that prioritize data-driven decision-making and the ongoing digital transformation within the financial sector.
The central business question addressed by this project is:
"How can banks effectively monitor the performance, distribution, and profitability of their loan portfolios to improve decision-making and manage financial risk?"
This project solves a common problem faced by financial institutions which is lack of visibility into the performance of various loan segments over time. Traditional reporting methods are often slow, inflexible, and fail to capture the real-time shifts in borrower behavior, loan quality, and profit generation. By addressing this, the project offers an opportunity to improve risk assessment, resource allocation, and strategic planning.

The goals of this project are to:

- Build an interactive, user-friendly dashboard that visualizes key metrics related to bank loan performance.
- Provide insights into loan profitability, distribution by sector or region, receivables over time, and more.
- Help stakeholders identify patterns and potential risks in their lending activities.
- Support data-driven decisions to improve the bank’s overall financial health and operational efficiency.

The bank benefits from this project by gaining:

- A centralized and intuitive tool to monitor key performance indicators (KPIs).
- Enhanced visibility into loan trends, helping prioritize profitable loan types or identify underperforming areas.
- Faster and more informed decision-making for loan approvals, risk management, and resource deployment.
- Support for regulatory compliance through transparent and up-to-date reporting capabilities.

## Data Overview

The dashboard acts as a strategic asset that supports smarter, faster, and more sustainable lending decisions. To achieve this, three datasets were integrated and modeled:

- Loan Details
- Client Details
- Loan Repayment Details

These datasets were linked through appropriate primary and foreign key, enabling a unified data model suitable for in-depth exploration of the bank's financial health and risk exposure.

#### Loan Details Table

Captures granular information about each loan issued, including amount disbursed, interest rate, credit score, loan type, repayment schedule, and various profitability indicators.

|Column Names| Description|
|------------|------------|
|Loan ID|A unique identifier for each loan issued. This serves as the primary key of the dataset.|
|Client ID|A unique identifier for each client. This serves as a foreign key, linking loans to individual clients.|
|Loan Amount Disbursed|The loan amount (in USD) disbursed to the client at the time of issuance.|
|Loan Type|The category of the loan issued. Possible values include: Term Loan, Merchant Cash Advance, Equipment Loan, Commercial Real Estate Loan, Line of Credit, and Invoice Financing.|
|Loan Tenure (Months)|The duration of the loan in months.|
|Loan Tenure (Years)|The duration of the loan in years.|
|Credit Score|The credit score assigned to the client company at the time of loan issuance, used to assess creditworthiness.|
|Loan Issue Date|The date on which the loan was issued to the client.|
|Loan Status|The current status of the loan. Values include Active (ongoing loans), Closed (fully repaid loans), and Defaulted (loans with 70–80% missed installments).|
|Interest Rate|The interest rate applied to the loan.|
|Maturity Date|The final due date by which the loan, including principal and interest, is to be fully repaid.|
|Monthly Installment Amount|The fixed monthly payment the client is obligated to make towards loan repayment.|
|Total loan Repayment Amount|The total sum, including principal and interest, that the client is expected to repay.|
|Funding Rate|The rate used to determine the funding amount provided by the bank.|
|Funding Amount|The total amount the bank allocates to fund the loan.|
|Expected Default Rate|The predicted percentage likelihood of a loan defaulting.|
|Loan Loss Provision Amount|The amount reserved by the bank to offset potential losses from defaulted loans. Calculated as: Expected Default Rate × Total Loan Amount.|
|Loan Recovered Amount|The amount successfully recovered from the client by the bank.|
|Outstanding Balance|The remaining loan balance yet to be paid by the client. Calculated as: Total Loan Repayment Amount − Loan Recovered Amount.|
|Total Liabilities|The total financial obligations or debts owed by the company.|
|Total Interest Expected Earnings|The projected interest earnings from the loan, based on the agreed-upon terms.|
|Total Interest Earned|The actual interest income realized by the bank from the loan.|
|Bank Profitability|The net profit generated by the bank from its lending operations.|
|Credit Score Range|The categorical range in which the client’s credit score falls, used for segmentation and risk assessment.|


#### Client Details Table

|Column Names| Description|
|------------|------------|
|Client ID|A unique identifier for each client. This serves as the primary key of the table.|
|Client Name|The official name of the client company.|
|Business Type|The industry classification of the client’s business. Categories include: Technology and IT Services, Hospitality and Tourism, Construction and Real Estate, Energy and Utilities, Transportation and Logistics, Retail and E-Commerce, Healthcare and Pharmaceuticals, and Manufacturing.|
|Annual Revenue|The total revenue generated by the company in a fiscal year.|
|Credit Score|A numeric representation of the client company’s creditworthiness.|
|Business Tenure|The number of years the company has been in operation.|
|Business Tenure Category|A categorical classification of business tenure based on the number of years in operation.|
|Total Expenses|Annual operational expenses incurred by the company|
|Total Assets|The total value of assets held by the company.|
|State|The full name of the U.S. state where the client company is located.|
|State (Short Form)|The official two-letter abbreviation of the U.S. state.|
|Net Profit|The company’s net profit, calculated as revenue minus total expenses and other deductions.|
|Total Liabilities|The total financial obligations or debts owed by the company.|
|DTI Ratio|The Debt-to-Income (DTI) ratio, which measures the company’s debt relative to its income an important indicator of financial health.|
|Profitability Ratio|A financial metric that evaluates the company’s ability to generate profit relative to its revenue, assets, or equity.|




#### Loan Repayment Details Tables

|Column Names| Description|
|------------|------------|
|Repayment ID|A unique identifier for each repayment transaction made by client companies. This serves as the primary key of the table.|
|Loan ID|The unique identifier of the associated loan. This acts as a foreign key linking the repayment to the corresponding loan in the loan data table.|
|Due Date|The scheduled date on which the monthly installment is expected to be paid by the client company.|
|Payment Date|The actual date on which the client company made the installment payment.|
|Payment Amount|The amount paid by the client company for a particular installment.|
|Monthly installment Amount|The agreed-upon installment amount that the client company is expected to pay each month as part of the loan repayment plan.|


## Dashboard Structure

The project consists of four main dashboard pages, each designed to highlight a specific aspect of the loan portfolio performance:
- Overview Page
- Allocation Page
- Receivables Page
- Ledger Page

### Overview Page
The Overview Page provides a high-level summary of the loan portfolio, offering insights into the distribution, status, and key metrics of the loans. It features visualizations like a map showing state-wise loan distribution, a bar chart depicting loan issuance by industry, and a matrix table summarizing financial data based on loan status (Active, Closed, Defaulted). These visualizations help users quickly assess the health and trends within the loan portfolio, making it easier to identify key patterns and areas requiring attention.

<img width="796" alt="Overview" src="https://github.com/user-attachments/assets/3daf4e83-f033-40ee-ac0e-9bc28896e1d6" />


#### 1. Map Visualization: Geographic Distribution of Loans by State
A dynamic, interactive map highlights the distribution of loans across various U.S. states. The visualization provides insight into two key metrics for each state:

**Loan Volume:** The number of loan applications issued in each state.

**Total Disbursement Amount:** The cumulative loan amount disbursed by the bank in each region.

This geographic analysis allows decision-makers to quickly identify high-performing or under-penetrated regions, enabling better resource allocation, marketing strategies, and risk evaluation based on regional exposure.

#### 2. Bar Chart: Loan Issuance by Industry (Business Type)

This bar chart breaks down loan disbursements across different industries, as defined in the "Business Type" category. The industries include sectors such as: Technology and IT Services, Hospitality and Tourism, Construction and Real Estate, Retail and E-Commerce, Healthcare and Pharmaceuticals, Transportation and Logistics, among others.

This visualization helps the bank understand which sectors are receiving the highest financial support and can be used to:

- Assess credit risk concentration across industries.
- Identify potential growth sectors or those in need of financial intervention.
- Align loan offerings with sector-specific demand trends.

#### 3. Matrix Table: Financial Summary by Loan Status

A structured matrix table provides a summarized financial breakdown by loan status—Active, Closed, and Defaulted. Each status represents a different phase or outcome of a loan and allows for side-by-side comparison of performance indicators. Key performance metrics displayed include:

**Number of Loan Applications:** Total count of loans issued under each status.

**Total Loan Amount Disbursed:** Aggregate value of loans sanctioned.

**Total Loan Payable:** The total repayment amount (including interest) expected from borrowers.

**Total Amount Received:** The cumulative amount recovered by the bank.

**Average Interest Rate:** The mean interest rate for loans within each status group.

**Average DTI (Debt-to-Income) Ratio:** An important creditworthiness indicator, reflecting the average debt burden relative to income for clients in each category.

**Average Profitability Ratio:** Indicates the average profitability of businesses in each status group, helping assess the financial health of clients and its impact on repayment.

By combining these metrics, the matrix table not only supports credit risk evaluation but also highlights repayment behavior patterns, client financial health, and performance of different loan products across their lifecycle.


### Allocation Page

**Allocation Page: Loan Allocation and Profitability Analysis**

The Allocation Page of the dashboard provides a detailed breakdown of the loan portfolio in terms of product allocation and corresponding profitability. This section is designed to help stakeholders understand how financial resources are distributed across loan types and how each product contributes to the bank’s bottom line. This section of the dashboard not only enables product-level analysis but also links operational decisions with financial performance. It empowers the bank’s strategic teams to refine loan offerings, optimize capital allocation, and maximize profitability. 

<img width="796" alt="Allocation" src="https://github.com/user-attachments/assets/df624733-5920-4884-bc44-531dd09d94e4" />


#### 1. Bar Chart: Number of Loans Issued by Loan Type

This vertical bar chart displays the total number of loans issued, categorized by Loan Type. The loan types include Term Loan, Merchant Cash Advance, Equipment Loan, Commercial Real Estate Loan, Line of Credit, Invoice Financing
This visualization helps identify which loan products are most frequently issued, providing insights into customer preferences, market demand, and potential focus areas for future growth or product development.

#### 2. Horizontal Bar Chart: Total Disbursed Amount by Loan Type

While the number of loans shows product popularity, the total disbursed amount reflects financial impact. This horizontal bar chart illustrates the aggregate amount disbursed for each loan type, offering a clearer view of capital allocation.

This chart is particularly useful for:
- Assessing which loan categories consume the most financial resources.
- Comparing issuance volume with disbursement size to identify high-value vs. high-volume products.
- Monitoring risk exposure across different loan products.


#### 3. Profitability Chart: Bank Profit by Loan Type

This chart visualizes the total profit earned by the bank from each type of loan product. Profit is calculated after accounting for interest income, loan repayments, and associated operational and risk-adjusted costs (such as defaults and provisions).

Key business insights from this chart include:

- Identification of the most profitable loan segments.
- Determining if high-disbursement loan types are yielding expected returns.
- Supporting strategic decisions around promoting or optimizing specific loan products.

#### 4. Treemap: Loan Distribution by Term Length (in Months)

The treemap offers a visual breakdown of loan volume by loan tenure (measured in months). Each block represents a specific loan term, and the size corresponds to the number of loans issued for that tenure.

This visualization provides insight into:

- Popular loan durations among clients.
- Short-term vs. long-term loan trends.
- Tailoring financial products to align with common borrowing behaviors.


### Receivables Page

**Receivables Page: Monitoring Disbursement and Payment Trends**

The Receivables Page of the dashboard plays a critical role in analyzing the bank’s cash flow and revenue realization over time. It focuses on understanding the consistency and effectiveness of loan repayments, detecting early signs of financial stress among borrowers, and supporting liquidity planning. It provides a comprehensive view of cash movement through the lending lifecycle tracking how funds flow out through disbursement and return via repayments. It supports both operational execution and strategic oversight by offering data-driven insights into borrower behavior, payment discipline, and revenue realization patterns.

<img width="796" alt="Receivables" src="https://github.com/user-attachments/assets/f2afd483-330b-4a66-b4fd-a219f76bed29" />


This page includes three key visualizations:

#### 1. Line Chart: Monthly Loan Disbursement Trend

This line chart captures the total loan amount disbursed month over month, providing a historical view of how lending activity has evolved over time. It enables stakeholders to:

- Monitor the volume and seasonality of loan disbursements.
- Assess the impact of business cycles, policy changes, or economic conditions on lending activity.
- Identify months with higher capital deployment for capacity planning and resource optimization.

By observing these trends, decision-makers can fine-tune loan offerings, marketing efforts, and internal resource planning to align with customer demand cycles.


#### 2. Line Chart: Monthly Profitability Trend

This visualization presents the bank’s monthly profit over time. Profit is derived from interest income minus any losses or operational costs related to loan issuance and recovery. This chart offers valuable insights into:

- Earnings volatility and the effect of loan performance on profitability.
- Long-term growth or decline in net income from lending operations.
- Financial health and sustainability of the loan portfolio.

This trend analysis is crucial for financial forecasting and helps in evaluating whether loan performance aligns with strategic profit goals.

#### 3. Line & Area Chart Combination: Expected vs. Actual Monthly Installments

This chart compares the expected monthly installment payments (based on loan agreements) with the actual payments received from clients. It uses a line chart to plot the expected payments and an area chart to show the actual collections.

This dual visualization is particularly important for:

- Identifying repayment gaps or shortfalls that could indicate default risk or client cash flow issues.
- Monitoring collection efficiency over time.
- Detecting trends in late or missed payments, allowing for early intervention or risk mitigation.

By quantifying the deviation between expected and actual cash inflows, this chart helps the bank manage working capital, assess credit risk, and refine loan recovery strategies.


### Ledger Page

**Ledger Page: Comprehensive Tabular Loan Analysis**

The Ledger Page of the dashboard serves as a detailed analytical repository, offering a tabular view of all individual loans issued by the bank. Unlike the summary dashboards and visualizations on other pages, this section provides a granular, record-level perspective to facilitate in-depth analysis, auditing, and decision support at the transaction level. This page enhances the depth of analysis available in the dashboard by shifting from high-level visual summaries to detailed, actionable data. It empowers various stakeholders to take informed actions, enforce data governance, and align loan monitoring with institutional policies and performance goals.

<img width="796" alt="Ledger" src="https://github.com/user-attachments/assets/fdc15b91-b376-409c-a4f4-dbbc38ef93b3" />


This page is particularly useful for:

- Loan officers and analysts performing case-by-case evaluations.
- Risk and compliance teams conducting portfolio reviews or audits.
- Executives and managers requiring access to detailed loan attributes in a structured format.

**Key Columns and Their Purpose**

The table on the Ledger Page contains the following fields, each chosen to offer a well-rounded view of each loan’s profile, performance, and risk exposure:

**Loan ID:** A unique identifier for each loan issued, used to track individual loan records and link them across datasets.

**Client Name:** The name of the client company to whom the loan was issued, helping users quickly identify and cross-reference client-specific performance.

**Business Tenure:** Indicates the number of years the client company has been operational. This metric is critical for evaluating borrower maturity and risk—newer businesses may carry higher default risk.

**Credit Score:** A numerical assessment of the borrower’s creditworthiness. This serves as a key input for risk profiling and interest rate determination.

**Loan Type:** Specifies the nature of the loan issued (e.g., Term Loan, Line of Credit, Commercial Real Estate Loan). Understanding the distribution of loan types helps in segment-level performance assessment.

**Interest Rate:** The rate at which the loan was issued, directly impacting expected revenue and repayment obligations.

**Debt-to-Income (DTI) Ratio:** This financial ratio indicates the proportion of the borrower's income used to service debt. A high DTI ratio signals elevated financial stress and potential default risk.

**Loan Amount Disbursed:** The total principal amount funded by the bank for each loan, critical for exposure and balance sheet assessments.

**Repayment Totals:** The total amount repaid to date by the client. This includes both principal and interest components and allows tracking of repayment progress.

**Outstanding Balance:** The remaining amount that the client is obligated to pay. This figure is derived by subtracting the repayment total from the total payable amount (principal + interest). It is essential for cash flow planning and collections management.

**Utility of the Ledger Page**

**Filtering and Drill-Down:** Users can apply filters on various columns (e.g., Loan Type, State, Credit Score range) to perform targeted analyses.

**Compliance & Risk Reviews:** Enables identification of high-risk loans based on poor credit scores, high DTI ratios, or large outstanding balances.

**Client Management:** Facilitates a better understanding of individual client loan behavior and engagement history, useful for relationship managers and client servicing teams.

**Performance Auditing:** Allows auditors to track loan issuance and repayment histories, ensuring transparency and accountability.


### Key Performance Indicators (KPIs)

A central feature of the dashboard is the consistent presence of six high-level Key Performance Indicators (KPIs) displayed across all pages. These KPIs serve as core financial and operational metrics that offer immediate insight into the performance of the loan portfolio, and they dynamically update based on user-selected filters such as date range, loan type, business category, and geographical region.

By maintaining the same KPIs across all pages, users are enabled to perform cross-sectional comparisons and assess performance from multiple analytical angles—by status, by client segment, by loan type, or over time.

![image](https://github.com/user-attachments/assets/53465ffe-79ae-4b61-8395-8c6530a0f293)

**Total Loan Amount Disbursed:** Represents the aggregate principal amount of all loans issued by the bank. It provides a top-line view of the bank’s lending activity and financial exposure. Monitoring this KPI helps in understanding the scale of operations and supports capital allocation planning.

**Total Amount Received:** Indicates the total repayments collected from borrowers to date. This figure includes both principal and interest payments and is crucial for assessing cash inflows, loan recovery efficiency, and overall repayment health of the loan book.

**Average Interest Rate:** This is the mean interest rate applied across all issued loans. It reflects the general pricing of credit products and provides insight into the bank’s lending policy. A rising average rate could indicate riskier portfolios or changing market conditions.

**Average Debt-to-Income (DTI) Ratio:** Shows the average proportion of a borrower's income committed to debt repayment. A key indicator of borrower affordability and credit risk, it helps in assessing the overall financial stress of the client base. Higher average DTI ratios may warrant increased monitoring or stricter loan issuance criteria.

**Net Interest Margin (NIM):** NIM measures the bank’s profitability from interest-earning loans, calculated as the difference between interest income earned and the funding cost, relative to the disbursed loan value. This metric reflects how efficiently the bank is generating profits from its lending operations.

**Average Profitability Ratio:** This reflects the average net income margin across all client companies. It is derived from the ratio of net profit to total revenue, indicating the overall financial health and operational efficiency of borrowers. A higher profitability ratio implies lower likelihood of default and better repayment potential.


### Dynamic Interactivity with each KPI

**Interactive and filter-responsive:** Values automatically adjust based on filters applied in the dashboard, such as loan status, loan type, industry segment, time period, or region.

**Comparative:** Because KPIs appear uniformly across all dashboard pages, users can easily benchmark performance across different dimensions (e.g., defaulted vs. active loans, state-wise disbursements, industry-specific profitability).

**Actionable:** Each metric provides quick access to decision-critical insights that support strategic initiatives, risk mitigation, and portfolio optimization.
Including these KPIs throughout the dashboard ensures cohesive storytelling and actionable insights, enabling stakeholders from analysts to executives to make data-informed decisions confidently and consistently.



### Interactive Filters

To enhance the dashboard's flexibility and support targeted, user-driven analysis, a set of global interactive filters is applied across all dashboard pages. These filters allow users to dynamically segment the loan portfolio, tailor the visualizations, and drill down into specific subsets of the data. This ensures the dashboard is not only informative but also highly customizable for diverse analytical needs.

#### State Filter

**Type:** Multi-select dropdown

**Function:** Enables users to filter all metrics and visuals based on specific U.S. states.

**Use Case:** This is particularly useful for regional performance analysis, identifying high-risk or high-growth states, and comparing loan disbursement or profitability trends geographically.

**Example:** A user can select “California” and “Texas” to view loan performance exclusively in those states.

#### Business Type Filter

**Type:** Multi-select dropdown

**Function:** Allows filtering based on the industry classification of the client companies.

**Categories:**

- Technology and IT Services
- Hospitality and Tourism
- Construction and Real Estate
- Energy and Utilities
- Transportation and Logistics
- Retail and E-Commerce
- Healthcare and Pharmaceuticals
- Manufacturing

**Use Case**: Enables comparison of financial metrics across industries, such as identifying which sectors have higher default rates or yield higher profitability.

**Example:** Users can isolate data for “Retail and E-Commerce” to evaluate loan performance trends specific to that industry.

#### Credit Score Range Filter

**Type:** Categorical filter with three predefined credit score brackets

**Ranges:**

- 750–850 (Excellent Credit)
- 700–749 (Good Credit)
- 650–699 (Fair Credit)
  
**Function:** Allows users to explore loan behavior and risk profiles based on borrower credit quality.

**Use Case:** Ideal for risk-based analysis. For example, users can examine whether lower credit score clients have higher default rates or if higher score borrowers contribute more to profitability.

**Example:** Filtering by “650–699” enables a focused view of higher-risk loans and their performance patterns.

#### Purpose and Benefits

These filters empower users to perform segmented analysis and derive insights that are context-specific and actionable. They promote better understanding of risk, return, and client demographics across various dimensions of the loan portfolio. Filters work in tandem with dynamic KPIs, charts, and tables, ensuring that all visual components of the dashboard respond synchronously to the applied filters. This interactivity transforms the dashboard into a self-service BI tool, supporting use cases across strategy, compliance, risk management, and lending operations. Including these filters enhances the dashboard's usability, personalization, and analytical power, ensuring that stakeholders from different business functions can extract the insights most relevant to their objectives

### Navigation and User Experience

To improve usability, custom navigation buttons were added to enable seamless switching between the dashboard pages. This allows users to easily explore different dimensions of the loan portfolio without needing to return to the main menu or external links.

To enhance dashboard usability and ensure a streamlined analytical workflow, custom navigation buttons have been implemented across all pages. These buttons are prominently positioned and styled for easy access, allowing users to switch between different analytical views without needing to return to a homepage or interact with external menus.

Key Features:

- Page-to-page navigation: Users can move directly from one dashboard section (e.g., Allocation) to another (e.g., Receivables or Ledger) using intuitive navigation controls.
- Consistent layout: Navigation buttons are available on all pages, maintaining a consistent user interface and experience.
- Improved accessibility: Reduces the need for manual page selection, enabling quicker access to desired insights and enhancing overall productivity.

Encourages deeper data exploration by minimizing friction. Facilitates cross-sectional comparisons by allowing users to switch perspectives quickly. Enhances the dashboard’s overall intuitiveness and user-friendliness, particularly for non-technical stakeholders.


### Results

**Top States by Loan Volume**

- Colorado
- North Dakota
- Arkansas
- Pennsylvania
- South Carolina

**Industries with large loan disbursement**

- Hospitality and Tourism
- Healthcare and Pharmaceuticals


**Risk and Profitability Pattern**

Defaulted Loans are associated with

- High Debt-to-income ratios
- Lowest Profitability Ratios

The following companies are likely defaulters due to high DTI ratio

- Smith PLC
- Shield, Jones and Flores
- Rivera
- Smith Limited
- Harell, Walten and Miller

**Loan Types**

- Most popular loan type is Merchant Cash Advance
- Least issued product is Line of Credit
- Commercial Real Estate loan is 2nd most issued loan type but has lowest bank profitability in monetary value.

**Industry Profitability**

Manufacturing:

- Lowest disbursement amount: $17 million
- High profitability ratio: 11.49%

Most Profitable Industries

- Transportation and Logistics
- Manufacturing
- Energy and Utilities

**Loan Volume and Profitability Trends**

- Highest disbursement month: February
- Decline in disbursements: March to May (likely due to policy tightening or macroeconomic caution)
- Recovery in trend: June
- Profitability decline despite full installment payments: New loans issued late in the year (e.g., November) contribute fewer payments (only December), lowering annual profitability despite incoming payments

**Profitability Metrics**

- Total loan amount disbursed: $202.9 million
- Total amount received: $67 million
- Average interest rate: 8.80%
- Average DTI: 4.71%
- Net interest margin: 7.19%
- Profitability ratio: 9.78%


**Most Profitable Loan Types**

- Merchant Cash Advance
- Invoice Financing
- Line of Credit
