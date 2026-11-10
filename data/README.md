# Dataset files

The project uses a synthetic e-commerce dataset with approximately 5 million records covering 2021–2025.

The CSV files are hosted on Google Drive because each is larger than GitHub's 100 MB regular-file limit:

- **[Download raw dataset (CSV)](https://drive.google.com/file/d/16vVBBc6QGaXNmqw3Wma9OAMbddJ4IJbe/view?usp=sharing)**
- **[Download cleaned dataset (CSV)](https://drive.google.com/file/d/1OR-DhpYlfooE0K9tIJ3kLkSVdC8DFGea/view?usp=sharing)**

To reproduce the workflow, download the raw CSV and place it at the input path expected by the scripts. Review paths in each script before execution; the cleaning scripts do not all write to the same destination.

The intermediate `data/processed/` directory was empty when the project was packaged.
