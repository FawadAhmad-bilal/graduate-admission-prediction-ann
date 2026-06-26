# 🎓 Graduate Admission Prediction using ANN

Predicting the probability of graduate school admission based on academic profile using an Artificial Neural Network built with Keras and TensorFlow.

---

## 📌 Problem Statement

Given a student's academic and profile data (GRE score, TOEFL score, GPA, etc.), predict their **chance of admission** to a graduate program. This is a **regression problem** — the output is a continuous value between 0 and 1.

---

## 📊 Dataset

- **Source:** [Kaggle — Graduate Admissions Dataset](https://www.kaggle.com/datasets/mohansacharya/graduate-admissions)
- **Size:** 500 rows × 8 features
- **Target:** `Chance of Admit` (ranging from 0 to 1)

| Feature | Description |
|---|---|
| GRE Score | Out of 340 |
| TOEFL Score | Out of 120 |
| University Rating | Out of 5 |
| SOP | Statement of Purpose Strength (out of 5) |
| LOR | Letter of Recommendation Strength (out of 5) |
| CGPA | Undergraduate GPA (out of 10) |
| Research | Research Experience (0 or 1) |

---

## 🧠 Model Architecture

```
Input Layer  → 7 features
Hidden Layer 1 → 120 neurons, ReLU activation
Hidden Layer 2 → 10 neurons, ReLU activation
Output Layer → 1 neuron, Linear activation (regression)
```

- **Loss Function:** Mean Squared Error (MSE)
- **Optimizer:** Adam
- **Epochs:** 100
- **Validation Split:** 20%

---

## ⚙️ Workflow

```
Data Loading → EDA → Drop Serial No. → Train/Test Split
→ MinMaxScaler → ANN Model → Training → Evaluation
```

1. Load dataset and perform basic EDA (`head`, `info`, `describe`)
2. Drop non-informative column (`Serial No.`)
3. Split into features `X` and target `y`
4. Train/Test split (80/20)
5. Scale features using **MinMaxScaler**
6. Build and train ANN
7. Evaluate using **R² Score**

---

## 📈 Results

| Metric | Value |
|---|---|
| R² Score | ~0.82+ |

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Keras](https://img.shields.io/badge/Keras-Sequential-red)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-preprocessing-green)
![Pandas](https://img.shields.io/badge/Pandas-EDA-lightblue)

---

## 🚀 How to Run

```bash
# Clone the repo
git clone https://github.com/FawadAhmad-bilal/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install tensorflow scikit-learn pandas numpy matplotlib

# Run the notebook
jupyter notebook Graduate_Admission_Prediction_using_ANN.ipynb
```

---

## 📁 Project Structure

```
├── Graduate_Admission_Prediction_using_ANN.ipynb
├── Admission_Predict_Ver1.1.csv
└── README.md
```

---

## 🔗 Related Projects

- [MNIST Digit Classification using ANN](../mnist_classification/)
- [Customer Churn Prediction using ANN](../customer_churn/)

---

## 👤 Author

**Fawad Ahmad**  
BS Artificial Intelligence — University of Haripur  
[GitHub](https://github.com/FawadAhmad-bilal)
