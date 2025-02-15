# Bangalore Home Price Prediction 🏠📈

A machine learning project to predict residential property prices in Bangalore using regression techniques.  
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/kalp12/Banglore-Home-Prices-prediction-using-ml)  

## Features ✨
- **Data Analysis**: Cleaned and preprocessed Bangalore property dataset
- **Price Prediction**: ML model with **85%+ accuracy** (R² score)
- **Feature Importance**: Identified key factors affecting property prices
- **Web Interface**: Flask-based UI for easy predictions *(if deployed)*
- **Scalable**: Handles 10,000+ data points efficiently

## Tech Stack 🛠️
- **Programming**: Python, JavaScript, HTML, CSS
- **Machine Learning**: Scikit-learn, Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Web Framework**: Flask
- **Cloud Platforms:**: AWS
- **Dataset**: Bangalore House Price Data (CSV)

## Installation 💻

### 1. Clone Repository
```bash
git clone https://github.com/kalp12/Banglore-Home-Prices-prediction-using-ml.git
cd Banglore-Home-Prices-prediction-using-ml
```
### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate    # Windows
```
### 3. Install Dependencies
```bash
pip install -r requirements.txt
```
### Usage 🚀
Run Jupyter Notebook
```bash
jupyter notebook bangalore_housing_analysis.ipynb
<!--Train Model-->
from model import train_model
model = train_model('data.csv')
<!--Make Prediction (Sample Input)-->
# Format: [total_sqft, bath, location_encoded, bhk]
sample_input = [[1250, 2, 45, 2]] 
predicted_price = model.predict(sample_input)
print(f"Predicted Price: ₹{predicted_price[0]:,.2f}")
```
Start Flask App
```bash
python app.py
Visit http://localhost:5000
```
Project Structure 📂

    Banglore-Home-Prices-prediction-using-ml
        ├── client/                                    #UI
        │   ├── app.html        
        │   └── app.css    
        │   └── app.js 
        ├── model/     
        │   ├── banglore_home_prices_final.ipynb      # Jupyter notebooks
        │   └── banglore_home_prices_model.pickle     # Saved ML model
        │   ├── bengaluru_house_prices.csv            # Raw & processed datasets
        ├── nginx_files/             
        │   └── bhp.conf
        ├── server/             
        │   └── artifacts
        │   │   └── banglore_home_prices_model.pickle     # Saved ML model
        │   │   ├── columns.json            
        │   ├── server.py               # Flask web interface
        │   ├── util.py
        │   └── requirements.txt       # Dependencies
### Model Performance 📊
| Metric            | Score   |
|------------------|---------|
| **R² Score**     | 0.87    |
| **MAE**         | ₹8.2L   |
| **MSE**         | 1.2e13  |
| **Cross-Val Score** | 0.84    |
