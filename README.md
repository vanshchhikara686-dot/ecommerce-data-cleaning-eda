# E-commerce Data Cleaning & Exploratory Data Analysis

A large-scale, synthetic e-commerce analytics project built with Python and Power BI. The project demonstrates dataset generation, data profiling, cleaning, validation, exploratory analysis, and business reporting across **5 million records** covering **2021–2025**.

> **Data note:** The dataset is synthetic and intended for portfolio demonstration. Dashboard metrics describe this generated dataset, not a real company's results.

## Project at a glance

| Project detail | Description |
|---|---|
| Dataset size | Approximately 5 million records |
| Time period | 2021–2025 |
| Data type | Synthetic e-commerce transaction data |
| Main tools | Python, Pandas, NumPy, Matplotlib, Seaborn, Power BI |
| Processing | CSV chunk processing is used in selected scripts (100,000 rows per batch) |
| Analysis areas | Categories, products, cities, sales channels, customer segments, order status, payment methods, monthly revenue and discounts |

## Skills demonstrated

- **Python data analysis:** Python scripting, Pandas and NumPy for data manipulation and analysis.
- **Data cleaning and preparation:** handling large CSV files, data type checks, transformation and preparation of analysis-ready data.
- **Data profiling and validation:** inspecting dataset structure, checking data quality and validating cleaned outputs.
- **Exploratory data analysis (EDA):** grouping, aggregation, trend analysis and comparative analysis across business dimensions.
- **Large-file processing:** using chunk-based CSV processing in selected scripts to work with large datasets.
- **Data visualization:** creating analytical charts with Matplotlib and Seaborn.
- **Business intelligence:** building Power BI report views and presenting KPIs through dashboards.
- **Business insight communication:** translating analytical summaries into findings about sales, customers, products and operations.

## Key project findings

The following findings are taken from the project's saved analytical CSV outputs and dashboard screenshots. Since the dataset is synthetic, these figures demonstrate the analysis workflow and should not be interpreted as actual company performance.

| Analysis area | Finding | What it indicates |
|---|---|---|
| Dataset scale | Approximately **5 million records** across **2021–2025** | The workflow was designed to explore a large, multi-year dataset. |
| Sales channels | Marketplace: **1,656,021** orders; Mobile App: **1,654,576**; Website: **1,654,449** | Order volumes are very evenly distributed across the three channels. |
| Product categories | Beauty has the highest category revenue in the saved summary (**~100.16bn**); Fitness is lowest (**~99.91bn**). | Category revenue is closely balanced in this synthetic dataset. |
| Order status | Returned **25.02%**; Processing **25.00%**; Cancelled **24.99%**; Delivered **24.99%** | Each order status accounts for approximately one-quarter of the records. |
| Payment methods | Net Banking has the largest share (**20.03%**); Cash on Delivery the smallest (**19.98%**). | Payment-method usage is almost evenly distributed. |
| Customer segments | New customers have the highest revenue in the segment summary (**~150.28bn**); Loyal customers have the lowest average order value (**~120.74K**). | Revenue and average order value are similar across the four customer segments. |
| City performance | Mumbai leads the saved city revenue summary (**~49.60bn**), followed by Delhi (**~49.58bn**). | Revenue is closely grouped among the top cities. |
| Monthly revenue | The highest month in the monthly summary is **August 2025 (~1,028.77 crore)**; the lowest is **February 2021 (~916.59 crore)**. | Monthly revenue varies over time, with a recurring lower level in February in the generated data. |

> **Interpretation note:** The saved category, channel, segment and city summary files show aggregates that do not reconcile to the total revenue displayed in the Power BI screenshot. These outputs are therefore presented as separate exploratory summaries, not as a reconciled financial statement. Dashboard figures are displayed as shown in the report and have not been independently audited against the PBIX model.

## Repository contents

```text
ecommerce-data-cleaning-eda/
├── data/
│   └── README.md
├── scripts/
│   └── README.md
├── outputs/
│   ├── category_discount/
│   └── eda/
├── powerbi/
│   ├── screenshots/
│   └── README.md
├── requirements.txt
├── .gitignore
└── README.md
```

The full raw and cleaned CSV files and the Power BI `.pbix` file are hosted on Google Drive because they exceed GitHub's regular file-size limit. Use the download links in the [data folder](data/README.md) and [Power BI folder](powerbi/README.md).

## Python workflow

1. **Generate** the synthetic e-commerce dataset.
2. **Inspect and profile** the generated data.
3. **Clean** the dataset and produce a cleaned version.
4. **Validate** the cleaned output.
5. **Explore** the data and generate analytical summaries and charts.
6. **Report** the business metrics in Power BI.

The Python scripts are organized by task in the `scripts/` directory. See [scripts/README.md](scripts/README.md) for the script inventory and execution notes.

## Power BI dashboard

**[Download the Power BI dashboard (.pbix)](https://drive.google.com/file/d/15HWfy3aTZqxK-oQ7euWUkxLIZj1eceCa/view?usp=sharing)**

The Power BI report is hosted on Google Drive because the `.pbix` file exceeds GitHub's regular file-size limit. The link is also recorded in [powerbi/dashboard file link](powerbi/dashboard%20file%20link).

### Dashboard screenshots

The following screenshots provide a preview of the report:

![Power BI dashboard preview 1](powerbi/Screenshot%202026-11-09%20143050.png)

![Power BI dashboard preview 2](powerbi/Screenshot%202026-11-09%20143115.png)

![Power BI dashboard preview 3](powerbi/Screenshot%202026-11-09%20143139.png)

The Power BI report contains three dashboard views represented by the supplied screenshots:

### E-commerce overview
- Total revenue: **149.96bn**
- Total orders: **5M**
- Delivered orders: **1M**
- Average order value: **120.88K**
- Monthly revenue trend from 2021 to 2025
- Revenue by product category

### Sales and customer analysis
- Revenue by sales channel
- Revenue by customer segment
- Orders by order status
- Top 10 products by revenue
- Revenue by city
- Product-name filter

### Payment analysis
- Orders by payment method

These are displayed values from the supplied dashboard screenshots; the underlying Power BI measures have not been independently audited.

## Reproducing the project

1. Install Python 3.10 or later.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Obtain the raw dataset and place it at the path expected by the generation/cleaning scripts, or generate it using the dataset-generation script.
4. Run the scripts in the intended workflow. Check each script's input and output paths before execution, because some scripts use project-relative paths and the cleaning scripts have different output destinations.
5. Review the CSV summaries and charts in `outputs/`.

**Important:** This repository documents the scripts and workflow. The entire pipeline has not yet been verified as a single clean run on a fresh machine. In particular, check the output path used by `clean_dataset.py` against the input path expected by downstream analysis scripts.

## Large data and report files

GitHub blocks regular files larger than 100 MB. The raw dataset, cleaned dataset, and Power BI report are therefore hosted on Google Drive. Their download links are provided in the respective folder documentation.

## Limitations and interpretation

- All records are synthetic.
- Dashboard totals and averages are specific to the generated dataset.
- Revenue and average order value are shown using the units/formats configured in the Power BI report; confirm the intended currency and aggregation definitions before interpreting them as real-world financial measures.
- Chunk processing is used by several scripts, but not every script is guaranteed to be memory-bounded. Review individual scripts before running on a machine with limited RAM.

## Author

**Vansh**  
GitHub: [@vanshchhikara686-dot](https://github.com/vanshchhikara686-dot)
