# Car Reviews via LLMs (Prototype)
<img src="car.jpeg">

This repository contains a Jupyter notebook (`llm.ipynb`) that prototypes a chatbot/assistant using multiple pre-trained Hugging Face models to process car reviews and customer text. The notebook demonstrates several NLP functionalities useful for both customers and human agents.

Project attribution
- This project was completed as part of Datacamp's "AI Engineer for Associate Data Analyst" career track.

Features implemented in the notebook
- Data loading
  - Loads dataset from `data/car_reviews.csv` (semicolon-separated).
- Sentiment analysis
  - Model: `distilbert-base-uncased-finetuned-sst-2-english`
  - Uses `transformers` pipeline for sentiment prediction and computes Accuracy & F1 using `evaluate`.
- Translation (English → Spanish)
  - Model: `Helsinki-NLP/opus-mt-en-es`
  - Example translation of sentences and BLEU scoring against `data/reference_translations.txt`.
- Question Answering (QnA)
  - Model: `deepset/minilm-uncased-squad2`
  - Demonstrates context + question tokenization and answer extraction.
- Summarization
  - Model: `facebook/bart-large-cnn`
  - Produces summaries for reviews.
- Safety / style checks
  - Uses `evaluate` metrics: `toxicity` and `regard` to assess generated summaries.

Quick Demo
- Head to Google Colab and upload the notebook and data files to run the notebook in your browser.

Files & paths
- Notebook: `llm.ipynb`
- Dataset expected at: `data\car_reviews.csv` (semicolon-separated)
- Reference translations: `data\reference_translations.txt`

License / Attribution
- Models and libraries are used under their respective licenses (Hugging Face model cards, Apache/MIT/other). Check each model card for details.
