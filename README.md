# House-Price-Prediction

## Project Overview
This project aims to predict house prices based on the California Housing dataset using various machine learning models. The best-performing model was selected after hyperparameter tuning and deployed using Flask.

---

## Dataset
The **California Housing Dataset** was used for this project. It contains information on various housing features such as median income, house age, total rooms, total bedrooms, population, households, latitude, and longitude.

---

## Data Preprocessing
- Handled missing values
- Standardized numerical features using **StandardScaler**
- Split the dataset into training (80%) and testing (20%) sets

---

## Model Training & Evaluation

### Initial Model Performance:
| Model                     | R² Score | RMSE  | MAE  |
|---------------------------|---------|--------|--------|
| Linear Regression         | 0.576   | 0.746  | 0.533  |
| Random Forest             | 0.805   | 0.505  | 0.328  |
| Decision Tree             | 0.623   | 0.703  | 0.454  |
| Gradient Boosting         | 0.776   | 0.542  | 0.372  |
| Support Vector Machine    | 0.729   | 0.596  | 0.398  |
| K-Nearest Neighbors       | 0.669   | 0.659  | 0.446  |

### Hyperparameter Tuning Results:
- **Random Forest (Tuned)**  
  - **R² Score:** 0.806  
  - **RMSE:** 0.505  
  - **MAE:** 0.327  

- **Gradient Boosting (Tuned) - Best Model**  
  - **R² Score:** 0.823  
  - **RMSE:** 0.482  
  - **MAE:** 0.323  

Based on the evaluation metrics, **Gradient Boosting Regressor** was selected as the final model.

---

## Deployment
The model was deployed using **Flask** to provide a user-friendly web interface where users can input house features and get predicted prices.

### Steps:
1. Trained the model and saved it using **joblib**
2. Built a **Flask API** to serve predictions
3. Created an interactive **HTML & CSS** interface
4. Hosted the application

---

## How to Run the Project

### 1. Clone the Repository
```sh
git clone https://github.com/Bala-krishna1/House-Price-Prediction.git
cd House-Price-Prediction
```

### 2. Install Dependencies
```sh
pip install -r requirements.txt
```

### 3. Run the Flask App
```sh
python app.py
```
The app will be accessible at `http://127.0.0.1:5000/`.

---

## Future Enhancements
- Improve model accuracy with **more feature engineering**
- Deploy using **Docker** for better scalability
- Implement **deep learning models** for comparison

---

## Author
**Balakrishna**
