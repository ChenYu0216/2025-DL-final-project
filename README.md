# 2025-DL-final-project
本專案為修習長庚大學2025年深度學習所做，為參加kaggle的Natural Language Processing with Disaster Tweets競賽使用，競賽網址集資料詳見https://www.kaggle.com/competitions/nlp-getting-started
(若程式有參考他人之程式碼，備注於註解中)

EDA主要呈現於BERT_model classification.ipynb的程式碼中，對資料集進行探索

ptt_crawler.ipynb為外部資料的取得，但後續我們有用人工做部分非真實災難的資料剃除，此資料須自行加上target欄位才能作為其他程式外部資料的來源

在BERT_model classification.ipynb中，包含資料探索、資料清理和參數最佳化，並實作了BERT、distiBERT、RoBERTa、RoBERTa_large、DeBERTa、DeBERTa_large六種模型，以及ensemble model

Llmma_classification.ipynb中，包含資料清理以及Llama-2-7b的量化版模型(本程式使用Hugging Face上的模型，若要使用需自行註冊取得Token)，視覺化上，本程式使用wandb，因此若需視覺化部分需登入個人帳號


