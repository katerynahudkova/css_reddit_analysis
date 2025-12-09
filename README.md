### Project title
**Tradwife discourse analysis on Reddit data**

### Research summary
Over a 5-year period we collected and analyzed how the discourse evolved from a niche aesthetic into a politically polarized topic.
Using a dataset of 2 668 413 items from seven diverse subreddits, we investigated the transformation of the 'tradwife' phenomenon.

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
Run `01_comments_preprocessing.ipynb` and `01_submissions_preprocessing.ipynb`. These notebooks clean the raw text, handle missing values and merge submissions with comments.

**Run Analysis:**
Run the EDA notebook (`02_eda_analysis.ipynb`). This script performs:

  * series decomposition (trend & seasonality analysis).
  * analysis using VADER and TextBlob.
  * Statistical testing (GLM, Spearman correlation).

### Environment

The analysis requires **Python 3.8+**. Install the necessary libraries using pip:

```bash
pip install pandas numpy matplotlib seaborn scipy statsmodels vaderSentiment textblob
```

### Link to initial dataset

The initial raw dataset (collected from Academic Torrents and filtered for specific subreddits) is available here:

  * **Google Drive link:** [Dataset Download]([https://drive.google.com/file/d/1p6PlhyqfTsVbfLwQAYU9OLS6cvqrcu31/view?usp=drive_link](https://drive.google.com/file/d/1UCX1BXGJEDyJohzamw_mPKGevEMKo-_K/view?usp=share_link))

Note: The dataset covers the period of July 2019 - July 2023 (sampled months: Jan, Apr, Jul, Oct) plus Summer 2024 data.

### Files and folder structure

The repository is organized to follow the data processing pipeline:

```text
├── data/
│   ├── input/              #raw CSV files here
│   └── output/             #processed/merged CSVs will be saved here
├── notebooks/
│   ├── 01_comments_preprocessing.ipynb  #step 1: cleaning and merging both sources of data
│   ├── 01_submissions_preprocessing.ipynb  
│   └── 02_eda_analysis.ipynb        #step 2: exploratory analysis, visualization and stats
├── scripts/
│   └── 00_raw_data_extraction.py   #utility for converting Pushshift ZST dumps to filtered CSVs
├── README.md               #project documentation
└── requirements.txt        #Python dependencies
```

```
```
