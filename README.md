# 🎭 Real-Time Sentiment Analysis

In today's digital world, **understanding public sentiment in real time** is crucial for businesses, governments, and researchers.  
Over **500 million tweets** are sent per day – a goldmine of opinions and emotions.  

Existing sentiment tools often **ignore Arabic inputs or spoken language**, making them less effective in multilingual contexts.  
This project builds a system capable of analyzing **Arabic and English text/voice inputs** with high accuracy in real time.  

---

## 🎯 Objectives
- ✅ Predict sentiment from **text or voice inputs** in both **Arabic and English**.  
- ✅ Use **Twitter and review datasets** to train robust models.  
- ✅ Employ **translation APIs** & **speech-to-text** tools for non-English and voice inputs.  
- ✅ Deliver **real-time predictions** via a user-friendly **Streamlit interface**.  

---

## 🏗️ System Architecture
The system processes **user text/voice input**, detects its language, translates non-English text, and predicts sentiment using trained deep learning models.  

### Flow:
1. **User Input** → Text or Voice  
2. **Speech-to-Text** (for voice inputs)  
3. **Language Detection**  
4. If Arabic → Translate using **Google Translator API**  
5. **Sentiment Prediction** (BILSTM / GRU / BERT models)  
6. **Real-Time Output** → Sentiment displayed to the user  

---

## 📂 Data Collection
- Collected from **Kaggle**:  
  - **Twitter Sentiment Analysis Dataset**  
  - **Social Media Analysis Sentiment Dataset**  
- Total = **75,269 text inputs with sentiment labels**  

---

## 🧹 Data Preprocessing
- Removed nulls and duplicates  
- Fixed labels → { Negative: `0`, Neutral: `1`, Positive: `2` }  
- Cleaned text: removed **hashtags, URLs, emojis, mentions, &, \***  
- Converted to lowercase → tokenized → removed stop words → lemmatized  
- Combined into final dataset = **65,269 text inputs**  
- Tokenization & Padding: `vocab_size = 30,000`, `max_len = 100`  
- Used **pre-trained GLoVe embeddings** for embedding layer  
- Train/Validation/Test split: **87% / 10% / 3%**  

---

## 🧠 Models & Results
| Model   | Validation Accuracy |
|---------|----------------------|
| **BiLSTM** | 89.8% |
| **GRU**    | 86.0% |
| **BERT**   | 90.7% |

- Best performance: **BERT with 90.7% accuracy**  
- Deployed using **Streamlit** for real-time interaction  

---

## 🛠️ Tools & Libraries
- **Python** (PyTorch, NumPy, Pandas, Matplotlib)  
- **Hugging Face Transformers**  
- **Streamlit** (Deployment)  
- **Google Translator API** (Language Translation)  
- **Speech-to-Text APIs** (Voice Input Handling)  
- **Google Colab** (Training)  
- **Kaggle Datasets**  

---

## 🚀 Deployment
- Web app built with **Streamlit**  
- Supports **text & voice input**  
- Provides **instant sentiment prediction**  

---

## 🔮 Future Work
- 📈 Collect larger, more diverse datasets (especially in Arabic dialects)  
- 📷 Add **Computer Vision** (camera input for multimodal emotion recognition)  
- ☁️ Deploy on **cloud services** for large-scale real-time usage  
- 🎙️ Improve voice support for low-resource dialects  

---

# 📌 Key Contributions
✔️ Real-time **multilingual sentiment analysis**  
✔️ Supports **voice & text inputs**  
✔️ Integrated **translation + speech-to-text APIs**  
✔️ Achieved **90.7% accuracy with BERT**  
✔️ Deployed using **Streamlit** for interactive use  

---
