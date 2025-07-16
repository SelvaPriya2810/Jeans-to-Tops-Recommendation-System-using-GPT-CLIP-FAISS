
# AI-Powered Jeans-to-Tops Fashion Recommender 👖→👕

This project is an intelligent clothing recommendation system that suggests stylish tops based on a given jeans image using AI models. It combines vision and language understanding through **OpenAI’s GPT-4**, **CLIP**, and **FAISS** for fast, similarity-based matching.

---

## ✨ Features

- 👕 Recommends the top 5 best-matching tops for any uploaded jeans image
- 🧠 Uses **GPT-4** to generate a context-aware fashion prompt (e.g., casual, modern, smart)
- 🖼️ Extracts smart visual features using **CLIP** (image + text embedding model)
- ⚡ Matches AI features using **FAISS** vector similarity search
- 🧹 Cleans the dataset by auto-detecting and filtering **non-top** items (e.g., pants, jackets)

---

## 📂 Dataset

Dataset used: [Clothes Dataset by ryanbadai on Kaggle](https://www.kaggle.com/datasets/ryanbadai/clothes-dataset)

Structure:
```

Clothes\_Dataset/
├── Kaos/           # T-Shirts
├── Polo/           # Polo Shirts
├── Kemeja/         # Button-down Shirts
├── Jeans/          # Input category (used for testing)
...

````

---

## 🛠️ Technologies Used

- [OpenAI GPT-4](https://openai.com/gpt) — generates fashion prompts
- [CLIP (Contrastive Language–Image Pretraining)](https://openai.com/research/clip) — multimodal embeddings
- [FAISS](https://github.com/facebookresearch/faiss) — fast similarity search
- Python Libraries: `transformers`, `torch`, `faiss-cpu`, `PIL`, `matplotlib`, `numpy`

---

## 🚀 How It Works

1. **Input**: Randomly selects an image from the jeans folder.
2. **GPT**: Generates a natural language prompt like:
   > “Pair this with a fitted crop top or a casual button-down shirt.”
3. **CLIP**: Converts both the jeans image and GPT prompt into embeddings.
4. **Search**: Uses FAISS to find the 5 most compatible top images from the database.
5. **Filter**: Only tops are used (non-top items are automatically filtered using CLIP).
6. **Display**: The jeans and the 5 best-matched tops are displayed side by side.

---


## 📦 Setup Instructions

1. Clone the repo:
```bash
git clone https://github.com/yourusername/jeans-top-recommender.git
cd jeans-top-recommender
````

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Download the dataset:

```python
import kagglehub
path = kagglehub.dataset_download("ryanbadai/clothes-dataset")
```

4. Set your OpenAI API key:

```python
openai.api_key = "your-api-key"
```

5. Run the notebook:

```bash
jupyter notebook Fashion_Recommender.ipynb
```

---

## ✅ TODO (Optional Enhancements)

* [ ] Add UI with Streamlit for drag-and-drop image input
* [ ] Add outfit explanation using GPT
* [ ] Filter by occasion (formal, streetwear, etc.)
* [ ] Save user choices and learn from preferences

---

## 👗 Inspired By

This project was inspired by the idea of bringing **AI-powered personal stylists** to real-world fashion tasks.

---

