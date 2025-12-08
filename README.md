````markdown
### Project title
**Tradwife discourse analysis on Reddit data**

### Research summary
Over a 5-year period, we collected and analyzed how the discourse evolved from a niche aesthetic into a politically polarized topic.
Using a dataset of ~13.1 million items from seven diverse subreddits, we investigated the transformation of the 'tradwife' phenomenon.**

### Instructions on how to run notebooks
To reproduce the analysis, follow these steps:

**Clone the repository:**
```bash
git clone https://github.com/katerynahudkova/css_reddit_analysis.git
cd css_reddit_analysis
````

**Download the Data:**
Download the raw dataset from the link provided in section 5 and place the CSV files in the `data/input/` folder.

**Run Preprocessing:**
Run `01_data_preprocessing.ipynb`. This notebook cleans the raw text, handles missing values and merges submissions with comments.

**Run Analysis:**
Run the EDA notebook (`02_eda_analysis.ipynb`). This script performs:

  * series decomposition (trend & seasonality analysis).
  * analysis using VADER and TextBlob.
  * Statistical testing (GLM, Spearman correlation).

### Environment or Dependency Requirements

The analysis requires **Python 3.8+**. Install the necessary libraries using pip:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels vaderSentiment textblob
```

### Link to Initial Dataset

The initial raw dataset (collected from Academic Torrents and filtered for specific subreddits) is available here:

  * **Google Drive Link:** [Dataset Download](https://drive.google.com/file/d/1p6PlhyqfTsVbfLwQAYU9OLS6cvqrcu31/view?usp=drive_link)

Note: The dataset covers the period of July 2019 - July 2023 (sampled months: Jan, Apr, Jul, Oct) plus Summer 2024 data.

### Files and Folder Structure

The repository is organized to follow the data processing pipeline:

```text
├── data/
│   ├── input/              # Raw CSV files here
│   └── output/             # Saved processed/merged CSVs here
├── notebooks/
│   ├── 01_data_preprocessing.ipynb  # Step 1: Cleaning, merging and masking data
│   └── 02_eda_analysis.ipynb        # Step 2: Exploratory analysis, visualization and stats
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

```
```
