# InfiGen Assignment A — Data Analysis & NLP

**Candidate ID:** B211623  
**Project:** GenAI Analyst — Assignment A

## Project Overview

This project combines media/research articles and Twitter posts, cleans and standardizes the data, and applies Generative AI-based NLP to extract:

- Drugs
- Diseases
- Study names
- Topic classification
- Sentiment

## Topic Categories

- Efficacy-General
- Progression Free Survival (PFS)
- Overall Survival (OS)
- Safety-General
- Safety-Side Effects
- General Opinion
- Others

## Files

```text
InfiGen_Assignment_A_B211623_GitHub/
├── InfiGen_Assignment_A_GenAI_NLP_B211623.ipynb
├── README.md
├── data/
│   └── raw/
│       ├── Media_Research_Articles_Data.xlsx
│       └── Twitter_Posts_Data.xlsx
└── output/
    └── predictions_B211623.csv
```

## Result

The final prediction file contains **100 records**: 50 media/research records and 50 Twitter records.

## How to Run

1. Open the notebook in Jupyter Notebook, JupyterLab, or Google Colab.
2. Install the packages listed in the notebook.
3. Add your Gemini API key securely when prompted. **Do not commit API keys to GitHub.**
4. Run the notebook cells in order.
5. The final predictions are written to `output/predictions_B211623.csv`.

## Technologies

Python, Pandas, Google Gemini API, Pydantic, OpenPyXL, tqdm, Jupyter/Google Colab.

## Notes

This repository is prepared as a portfolio/showcase copy of the assignment. If the supplied assignment datasets are not permitted to be publicly redistributed, keep the `data/raw/` folder private or remove it before making the GitHub repository public.
