# Deep Learning Models for Customer Time-to-Repurchase Prediction  

This project explores deep learning architectures for predicting **the number of days until a customer’s next purchase** using the **Online Retail II** dataset.  

We compare **LSTM, CNN, TCN, CNN+LSTM, and CNN+TCN** models to determine which best captures short-term and long-term purchasing trends. The project highlights that **CNN-based models** provide highly accurate and computationally efficient solutions for time-to-event forecasting in retail.

---

## Project Structure
```
customer-repurchase-prediction/
│
├── GroupG_Implementation_Code.ipynb   # Jupyter notebook with full implementation
├── GroupG_Project_Report.pdf          # Detailed project report
├── README.md                          
```

---

## Key Features
- **Exploratory Data Analysis (EDA)** – Analyzes customer behavior, transaction frequency, and purchasing gaps.
- **Data Preprocessing** – Cleans, filters, and prepares data for sequence modeling.
- **Model Implementation** – Builds and trains:
  - LSTM  
  - CNN  
  - TCN  
  - CNN + LSTM (hybrid)  
  - CNN + TCN (hybrid)  
- **Evaluation Pipeline** – Compares models using **MAE**, **RMSE**, and **MedianAE**.
- **Deployment Considerations** – Code designed to be reusable and deployable via API (Flask/FastAPI).

---

## Installation & Setup

### Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/customer-repurchase-prediction.git
cd customer-repurchase-prediction
```

### Install Dependencies
Create a virtual environment (recommended) and install packages:

Example:
```
tensorflow
pandas
numpy
matplotlib
scikit-learn
```

---

## Results
| Model        | MAE     | RMSE    | MedianAE |
|-------------|---------|--------|---------|
| **CNN**      | **0.5824** | 3.9522 | **0.0580** |
| CNN + LSTM  | 0.5832 | 3.9520 | 0.0587 |
| CNN + TCN   | 0.5849 | 3.9515 | 0.0585 |
| LSTM        | 0.5856 | 3.9518 | 0.0614 |
| TCN         | 0.5950 | **3.9503** | 0.0707 |

**Key Insight:** CNN achieved the best overall performance with the lowest MAE and MedianAE, making it an ideal lightweight model for real-world deployment.

---

## How to Run
Open the Jupyter Notebook and execute step by step:
```bash
jupyter notebook GroupG_Implementation_Code.ipynb
```
Follow the cells to:
1. Load and preprocess the dataset  
2. Train the models  
3. Evaluate results  
4. Visualize predictions  

---

## Dataset
The project uses the **Online Retail II** dataset containing over **500,000 e-commerce transactions** from a UK-based retailer (2009–2011).  
Features include: `InvoiceDate`, `CustomerID`, `Quantity`, `Price`, `Country`.

---

## Future Work
- Add product category, seasonality, and demographic features  
- Tune hyperparameters (filter sizes, sequence length, learning rate)  
- Experiment with **attention mechanisms** for better sequence modeling  
- Deploy as a REST API (Flask/FastAPI) for real-time predictions  

---

## Contributors
- **Lin Myat Zaw Latt** – [x24121614@student.ncirl.ie](mailto:x24121614@student.ncirl.ie)  
- **Zin Win Phyo** – [x23402849@student.ncirl.ie](mailto:x23402849@student.ncirl.ie)  
- **Zuu Zuu Kyaw Shwe** – [x24106585@student.ncirl.ie](mailto:x24106585@student.ncirl.ie)  

---

## License
This project is developed as part of the **Deep Learning and Generative AI** module at **National College of Ireland**.  
You are free to use and modify for educational purposes.
