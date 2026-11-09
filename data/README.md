# Dataset files

The project uses a synthetic e-commerce dataset with approximately 5 million records covering 2021–2025.

The original raw CSV (approximately 644 MB) and cleaned CSV (approximately 641 MB) are not stored in this repository because each exceeds GitHub's 100 MB regular-file limit. No public download location has been configured yet.

To reproduce the workflow, place the raw data at the input path expected by the scripts, then run the generation/inspection and cleaning steps as appropriate. Review paths in each script before execution; the cleaning scripts do not all write to the same destination.

The intermediate `data/processed/` directory was empty when the project was packaged.
