# E-commerce Data Cleaning & Exploratory Data Analysis

A large-scale, synthetic e-commerce analytics project built with Python and Power BI. The project demonstrates dataset generation, data profiling, cleaning, validation, exploratory analysis, and business reporting across **5 million records** covering **2021–2025**.

> **Data note:** The dataset is synthetic and intended for portfolio demonstration. Dashboard metrics describe this generated dataset, not a real company's results.

## Project at a glance

- **Records:** 5 million
- **Period:** 2021–2025
- **Primary tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Power BI
- **Processing approach:** CSV chunk processing is used in several scripts, with a batch size of 100,000 rows.
- **Analysis areas:** sales channels, customer segments, products, cities, categories, order status, payment methods, monthly revenue, and category discounts.

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

The full raw and cleaned CSV files and the Power BI `.pbix` file are large (approximately 644 MB, 641 MB, and 221 MB respectively). They are not included in this initial GitHub upload. See [data/README.md](data/README.md) and [powerbi/README.md](powerbi/README.md) for the current availability notes.

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

GitHub blocks regular files larger than 100 MB. The full CSV datasets and Power BI report therefore need to be distributed through a suitable external storage location or Git LFS before they can be downloaded in full. No external download link is configured yet.

## Limitations and interpretation

- All records are synthetic.
- Dashboard totals and averages are specific to the generated dataset.
- Revenue and average order value are shown using the units/formats configured in the Power BI report; confirm the intended currency and aggregation definitions before interpreting them as real-world financial measures.
- Chunk processing is used by several scripts, but not every script is guaranteed to be memory-bounded. Review individual scripts before running on a machine with limited RAM.

## Author

**Vansh Chhikara**  
GitHub: [@vanshchhikara686-dot](https://github.com/vanshchhikara686-dot)
