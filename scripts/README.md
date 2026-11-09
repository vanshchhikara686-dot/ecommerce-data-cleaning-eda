# Python scripts

The project includes 16 Python scripts:

## Dataset creation, inspection, and cleaning
- `generate_dataset.py` — generates the synthetic dataset.
- `inspect_dataset.py` — inspects dataset structure and content.
- `profile_full_dataset.py` — profiles the full dataset.
- `clean_dataset.py` — first data-cleaning workflow.
- `clean_dataset_v2.py` — revised data-cleaning workflow.
- `final_validation.py` — validates the cleaned data.

## Exploratory and business analysis
- `exploratory_data_analysis.py`
- `category_discount_analysis.py`
- `channel_performance_analysis.py`
- `city_revenue_analysis.py`
- `customer_segment_analysis.py`
- `monthly_revenue_analysis.py`
- `order_status_analysis.py`
- `payment_method_analysis.py`
- `segment_aov_analysis.py`
- `top_products_analysis.py`

## Execution notes

Install the dependencies listed in the repository's `requirements.txt`. Run scripts from the project root so their relative paths resolve as intended. Inspect each script's input/output paths before running.

Several scripts use chunked CSV processing with a batch size of 100,000 rows. Do not assume every step is memory-bounded: the revised cleaning script loads the dataset into memory. The end-to-end pipeline has not yet been verified as a single fresh-machine run.
