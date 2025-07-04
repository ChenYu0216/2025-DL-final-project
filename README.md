# 2025-DL-final-project

本專案為長庚大學 2025 年深度學習課程的期末專案，參加了 Kaggle 上的「Natural Language Processing with Disaster Tweets」競賽。

競賽網址及資料集詳情請參考：[Kaggle: NLP - Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started)

---

## 專案結構
```
2025-DL-final-project/
├── BERT_model_classification.ipynb
├── Llama_classification.ipynb
├── mistral_classification.ipynb
  ├──requirement_for_mistral
├── ptt_crawler.ipynb
├── README.md
├── .gitignore
```

---


##  資料探索與前處理

- `ptt_crawler.ipynb`：用於爬取 PTT 上的災難相關討論，並進行初步資料清理，此資料作為訓練的外部資料，嘗試強化模型的泛化能力
- `BERT_model_classification.ipynb`：進行資料探索性分析（EDA）主要進行程式，其餘模型程式就無再進行EDA

---

## BERT類模型實作

在 `BERT_model_classification.ipynb` 中，實作了以下模型：

- BERT
- DistilBERT
- RoBERTa
- RoBERTa_large
- DeBERTa
- DeBERTa_large
- Ensemble 模型

並進行了超參數調整以提升效能。

---

## Llama-2-7b 模型實作

在 `Llama_classification.ipynb` 中，使用 Hugging Face 上的 Llama-2-7b 量化版模型進行分類。

**注意事項**：

- 需要在 Hugging Face 註冊帳號並取得 Token。
- 使用 Weights & Biases（WandB）進行視覺化，需登入帳號以查看訓練過程。

---

## Mistral 模型實作

在 `mistral_classification.ipynb` 中，實作了 Mistral 模型進行分類任務

模型建構參考:https://medium.com/@lukas.hauzenberger/multilabel-classification-using-mistral-7b-on-a-single-gpu-with-quantization-and-lora-8f848b5237f3

**注意事項**：

- 需要在 Hugging Face 註冊帳號並取得 Token。
- 使用 Weights & Biases（WandB）進行視覺化，需登入帳號以查看訓練過程。

---


## 注意事項

- 部分外部資料需手動處理，人工過濾，用人為觀察對應關鍵字找到的資料是否都是災難貼文(但以我們預設的關鍵字去做，需要剔除的資料量不大)
- 程式碼中若參考他人資料，已於註解中標明出處。
- 除Mistrial有特定numpy的版本定以外，其餘程式碼皆可直接在colab上運行以及安裝套件


