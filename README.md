# Brain Tumor Classification & Segmentation (Streamlit + Colab + Cloudflare Tunnel)

This project demonstrates how to run a **Streamlit app inside Google Colab** and expose it to the web securely using **Cloudflare Tunnel**.
The app focuses on **Brain Tumor Classification & Segmentation** using deep learning models on MRI images.

---

## 🚀 Features

* Brain Tumor **detection** (Benign, Malignant, or None).
* Tumor **segmentation** on MRI images.
* Interactive **Streamlit dashboard** for uploading and testing images.
* Run entirely on **Google Colab**, no need for local setup.
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
git clone https://github.com/your-username/brain-tumor-streamlit.git
cd brain-tumor-streamlit
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run on Colab

Upload the notebook to **Google Colab**, then run these cells:

```python
# Install Streamlit and Cloudflared
!pip install -q streamlit
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

* [LGG Segmentation Dataset](https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation)
* [Brain MRI Images Dataset](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-br)

---

## 📸 Screenshots

![Streamlit1](imagesStreamLit/screenshot1.png)
![Streamlit2_Result](imagesStreamLit/screenshot1.png)

---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you’d like to improve.

---

## 📜 License

This project is licensed under the MIT License.

---

👉 Do you want me to also create a **requirements.txt** file (with `streamlit`, `tensorflow`, `opencv-python`, etc.) so it’s ready for GitHub?
