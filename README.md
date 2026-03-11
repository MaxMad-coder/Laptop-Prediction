# 💻 Laptop Price Predictor

A **Machine Learning web application** built with **Streamlit** that predicts the price of a laptop based on its specifications. The model is trained on real laptop data and uses a pre-trained pipeline to deliver accurate price predictions in USD.

---

## 🖥️ Features

- 🔍 Predict laptop price based on 12 specifications
- 🏷️ Supports multiple brands, CPU, GPU, and OS types
- 📊 Two-column interactive UI built with Streamlit
- 💡 Calculates PPI (Pixels Per Inch) automatically from resolution and screen size
- 💰 Displays predicted price in USD
- ⚡ Instant predictions using a pre-trained ML pipeline

---

## 📸 Screenshots

> Add a screenshot of your app here after running it.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python 3 | Core programming language |
| Streamlit | Web application framework |
| Scikit-learn | Machine learning pipeline |
| NumPy | Numerical computations |
| Pandas | Data manipulation |
| Pickle | Load pre-trained model and data |

---

## 📁 Project Structure

```
laptop-price-predictor/
│
├── app.py                  # Main Streamlit application
├── pipe_object.pkl         # Pre-trained ML pipeline (model)
├── laptop_data.pkl         # Processed laptop dataset
├── laptop_data.csv         # Raw laptop dataset
├── laptopPrediction.ipynb  # Jupyter notebook (model training)
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/laptop-price-predictor.git
cd laptop-price-predictor
```

### 2. Create a Virtual Environment (Recommended)
```bash
python -m venv venv

# Activate on Windows
venv\Scripts\activate

# Activate on Mac/Linux
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install streamlit scikit-learn numpy pandas
```

Or use requirements.txt:
```bash
pip install -r requirements.txt
```

### 4. Run the Application
```bash
streamlit run app.py
```

App opens at:
```
http://localhost:8501
```

---

## 🚀 How to Use

1. Open the app in your browser
2. Fill in the **Basic Laptop Info** (left column):
   - Brand
   - Laptop Type
   - RAM
   - Weight

3. Fill in the **Advanced Laptop Info** (right column):
   - TouchScreen (Yes/No)
   - IPS Display (Yes/No)
   - Screen Size
   - Screen Resolution
   - Operating System
   - CPU Brand
   - GPU Brand
   - HDD Storage
   - SSD Storage

4. Click **"Predict Price"**
5. The predicted price will be displayed in **USD**

---

## 🧠 How the Model Works

```
User Input (12 features)
        │
        ▼
PPI Calculation
(X_res² + Y_res²)^0.5 / screen_size
        │
        ▼
Pre-trained ML Pipeline (pipe_object.pkl)
        │
        ▼
np.exp(predicted value)   ← log-inverse transform
        │
        ▼
Price in USD (x 0.012 conversion)
```

---

## 📊 Input Features

| Feature | Type | Options |
|---|---|---|
| Brand | Categorical | Dell, HP, Apple, Lenovo, etc. |
| Type | Categorical | Notebook, Gaming, Ultrabook, etc. |
| RAM | Numerical | 4, 6, 8, 12, 16, 24, 32, 64 GB |
| Weight | Numerical | 1.0 to 2.8 Kg |
| TouchScreen | Binary | Yes / No |
| IPS Display | Binary | Yes / No |
| Screen Size | Numerical | 13.3, 15.6, 17.3 inch |
| Resolution | Categorical | 1920x1080, 4K, etc. |
| OS | Categorical | Windows, Mac, Linux, etc. |
| CPU Brand | Categorical | Intel, AMD, etc. |
| GPU Brand | Categorical | Nvidia, AMD, Intel |
| HDD | Numerical | 0, 256, 512, 1024, 2048 GB |
| SSD | Numerical | 0, 128, 256, 512, 1024 GB |

---

## 📌 requirements.txt

```
streamlit
scikit-learn
numpy
pandas
```

---

## 📄 License

This project is open-source and free to use under the MIT License.

---

## 🙋 Author

**Your Name**
- GitHub: [@MaxMad-coder](https://github.com/MaxMad-coder)
- Email: manash212005@gmail.com
