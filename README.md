# 📚 Laptop Price Predictor

A machine learning web application built with **Flask** that predicts the **price of a laptop** based on its specifications like RAM, CPU, GPU, Operating System, and other features.

---

## 📂 Project Structure

```
Laptop-Price-Predictor/
├── static/
│   └── style.css             # CSS styling for the website
├── templates/
│   └── index.html             # HTML front-end template
├── model/
│   └── predictor.pickle       # Pre-trained machine learning model
├── app.py                     # Flask backend server
└── README.md                  # Project documentation (this file)
```

---

## 🚀 How It Works

1. **User** fills a web form with laptop specifications.
2. **Flask server** collects the data and prepares the feature list.
3. **Pre-trained ML model** (`predictor.pickle`) predicts the laptop price.
4. The **predicted price** (in LKR) is displayed on the website.

---

## 🛠️ Tech Stack

- **Python 3.8+**
- **Flask** (web framework)
- **HTML/CSS** (frontend)
- **Pickle** (for loading ML model)
- **NumPy** (for data processing)

---

## 🔍 Features

- Predicts laptop prices based on:
  - RAM size
  - Weight
  - Touchscreen or not
  - IPS panel or not
  - Brand (Company)
  - Laptop type (Notebook, Gaming, etc.)
  - Operating System (Windows, Mac, Linux, Other)
  - CPU brand
  - GPU brand
- Real-time prediction and price display.
- Fully responsive simple UI.

---

## 📥 How to Run Locally

> **Make sure Python and pip are installed**

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Laptop-Price-Predictor.git
cd Laptop-Price-Predictor
```

### 2. Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
```

Activate it:

- Windows:
  ```bash
  .\venv\Scripts\activate
  ```
- Mac/Linux:
  ```bash
  source venv/bin/activate
  ```

### 3. Install Requirements

```bash
pip install flask numpy
```

*(Note: You might add `scikit-learn` if retraining the model.)*

---

### 4. Run the Application

```bash
python app.py
```

- Go to `http://127.0.0.1:5000/` in your browser.
- Fill in laptop details and click **Predict Price**.

---

## 🧠 Model Training (Optional)

The `predictor.pickle` file is a **pre-trained regression model**.  
To train your own model:
1. Collect laptop dataset (with features like RAM, CPU, etc.).
2. Preprocess (one-hot encode categories, scale numerical fields).
3. Train a regression model (e.g., Random Forest, XGBoost).
4. Save model:

```python
import pickle
with open('model/predictor.pickle', 'wb') as file:
    pickle.dump(model, file)
```

---

## 📌 Important Notes

- Model predicts in **USD** internally, then multiplies by **221** to convert into **LKR** (approximate exchange rate used).
- This is a **basic project** to demonstrate ML+Flask integration, not production-grade.
- If you modify the form inputs, ensure the **input features match** what the model expects.

---

## 🤝 Contribution

Feel free to:
- ⭐ Star the repository
- 🐛 Report bugs
- 🌟 Suggest improvements

Pull requests are welcome!

---

## 📜 License

This project is open-source and free to use for educational purposes.

---

# 🎯 Summary

This project teaches:
- Frontend (HTML forms)
- Backend (Flask)
- Machine Learning model integration
- Basic web hosting of AI predictions
