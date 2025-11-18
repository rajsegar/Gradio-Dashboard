
<img width="381" height="132" alt="gar" src="https://github.com/user-attachments/assets/5fe78c40-59ac-4606-924e-2ce79ca88970" />


# Gradio-Dashboard
Gradio is an open-source Python package that simplifies the technique of constructing demos or web applications for machine learning models, APIs, or any Python function. With it, you may create demos or web applications while not having JavaScript, CSS, or web hosting experience.

# 🧪 

This repository provides a clean, production‑ready **Gradio Dashboard** for running inference on a fine‑tuned **DistilBERT sentiment classification model**. The model was trained using **TextAttack** on the Rotten Tomatoes dataset and supports both local CPU and GPU execution.

---

## 🚀 Features

* 🎛️ **Interactive Gradio UI** for quick testing
* 🔐 **Simple Authentication** included for controlled access
* ⚡ **GPU Acceleration** when available
* 📦 **Fully portable** — ideal for GitHub deployment or local use

---

## 📁 Project Structure

```
project/
│
├── gardio.py                   # Gradio dashboard script
├── outputs/                    # Folder containing fine‑tuned model
│   └── 2025-11-01.../best_model
└── README.md                   # Documentation (this file)
```

---

## 🛠️ Requirements

Ensure the following dependencies are installed:

```bash
pip install torch transformers gradio
```

Your project also requires the **fine‑tuned DistilBERT model** exported by TextAttack. Set its path in `gardio.py`:

```python
MODEL_PATH = r"outputs/2025-11-01-09-44-22-099720/best_model"
```

---

## ▶️ Running the Dashboard

Start the Gradio web app locally:

```bash
python gardio.py
```

You will be prompted for login credentials:

* **Username:** `admin`
* **Password:** `pass1234`

Once authenticated, the dashboard will open at:

```
http://127.0.0.1:7860/
```

---

## 🧩 Code Overview (gardio.py)

The script:

* Loads tokenizer + model from the fine‑tuned checkpoint
* Sends tensors to CPU/GPU depending on availability
* Wraps inference logic into a Gradio `Interface`
* Adds optional authentication using `same_auth()`

```python
import torch
from transformers import AutoTokenizer, AutoModelForSequenceClassification
import gradio as gr

MODEL_PATH = "outputs/.../best_model"
```

---

## 🖥️ Dashboard Preview

The dashboard presents:

* A textbox for user input
* Real‑time sentiment classification
* Confidence score per prediction

(You may add screenshots or GIFs here when uploading to GitHub.)

---

## 🔒 Authentication Logic

```python
def same_auth(username, password):
    return username == "admin" and password == "pass1234"
```

You can modify this to integrate:

* OAuth
* JWT
* Environment‑based secrets
* GitHub authentication

---

## 📦 Deployment Options

### 1. Local Machine

Just run:

```bash
python gardio.py
```


https://github.com/user-attachments/assets/3ec62208-2888-47ac-a29a-d0a56c57a131


## 🤝 Contribution

Feel free and join the social 

https://www.linkedin.com/in/rajsegar-alagarathnam/

* Fork the repo

---


