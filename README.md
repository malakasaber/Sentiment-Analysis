# Sentiment Analysis (Streamlit + Colab + Cloudflare Tunnel)

This project demonstrates how to run a **Streamlit app inside Google Colab** and expose it to the web securely using **Cloudflare Tunnel**.
The app focuses on **Sentiment Analysis of customer feedback and product reviews**, classifying text into **Positive, Negative, or Neutral** sentiments.

---

### [Colab Copy on Drive](https://colab.research.google.com/drive/1DwV4BPsRuOZJ35cw3TKLsBmOr0NdfRw2)

## 🚀 Features

* Sentiment **classification** of text (Positive / Negative / Neutral).
* Supports both **traditional ML (TF-IDF + LSTM)** and **transformer-based models (BERT, RoBERTa)**.
* Interactive **Streamlit dashboard** for real-time text input and prediction.
* Run entirely on **Google Colab**, no local setup required.
* Shareable **public URL** via Cloudflare Tunnel.

---

## 📂 Project Structure

```
├── app.py                # Streamlit app
├── notebook.ipynb        # Google Colab notebook
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
```

---

## 🛠️ Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/your-username/sentiment-analysis-streamlit.git
cd sentiment-analysis-streamlit
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run on Colab

Upload the notebook to **Google Colab**, then run these cells:

```python
# Install Streamlit and Cloudflared
!pip install -q streamlit scikit-learn transformers torch tensorflow
!wget -q https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64.deb
!dpkg -i cloudflared-linux-amd64.deb

# Start Streamlit
!streamlit run app.py &

# Expose via Cloudflare Tunnel
!cloudflared tunnel --url http://localhost:8501 --no-autoupdate
```

At the end, you’ll get a **public URL** to access your app 🎉.

---

## 📊 Dataset

* [Twitter Entity Sentiment Analysis Dataset](https://www.kaggle.com/datasets/jp797498e/twitter-entity-sentiment-analysis/data)

---

## 🧠 Models & Tools Used

* **Traditional ML:** TF-IDF + LSTM
* **Transformers:** BERT, RoBERTa (via Hugging Face)
* **Libraries:** Scikit-learn, Transformers, PyTorch, TensorFlow
* **Deployment:** Streamlit

---

## 📸 Screenshots

![Streamlit1](imagesStreamLit/screenshot1.png)
![Streamlit2\_Result](imagesStreamLit/screenshot2.png)

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss improvements.

---

## 📜 License

This project is licensed under the MIT License.

---

👉 Do you want me to also create a **requirements.txt** for you (with `streamlit`, `scikit-learn`, `transformers`, `torch`, `tensorflow`, etc.) so you can push it directly to GitHub?
