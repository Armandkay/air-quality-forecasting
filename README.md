# Air Quality Forecasting – Machine Learning Techniques I

## Project Overview

This project focuses on forecasting **PM2.5 air pollution levels** in Beijing using **Recurrent Neural Networks (RNNs)** and **Long Short-Term Memory (LSTM)** models. The goal is to leverage historical air quality and meteorological data to build predictive models that help governments and communities make informed decisions to mitigate pollution risks.

This assignment is part of the **Machine Learning Techniques I course**.

---

## Dataset

The dataset is provided via the Kaggle competition:

* **train.csv** – historical air quality and weather data for training
* **test.csv** – unseen data used for predictions
* **sample\_submission.csv** – format required for Kaggle submission

Key features include:

* Meteorological variables (temperature, pressure, wind speed, etc.)
* Air quality metrics (PM2.5, PM10, NO2, etc.)
* Time-series information (timestamps)

---

## Project Structure

```
air-quality-forecasting/
│── data/                 # Raw and processed datasets
│── notebooks/            # Jupyter notebooks for exploration & modeling
│   └── air_quality_forecasting.ipynb
│── src/                  # Python scripts for preprocessing & model training
│── outputs/              # Model predictions and logs
│── report/               # Final project report (Word/PDF)
│── submission.csv        # Kaggle submission file
│── README.md             # Project documentation
```

---

## Approach

1. **Data Exploration & Preprocessing**

   * Handled missing values
   * Generated input-output sequences with time windowing
   * Normalized features for better convergence

2. **Model Design**

   * Built and tested multiple **RNN/LSTM** models
   * Experimented with different hyperparameters (batch size, learning rate, hidden units, optimizers)
   * Evaluated performance using **RMSE (Root Mean Squared Error)**

3. **Experiments & Fine-Tuning**

   * Conducted systematic experiments with varied architectures
   * Selected the best-performing LSTM configuration

4. **Submission**

   * Generated predictions for the **test.csv** file
   * Formatted results according to `sample_submission.csv` and submitted to Kaggle

---

## Results

* Best Model: **LSTM with 2 hidden layers**
* Evaluation Metric: **Root Mean Squared Error (RMSE)**
* Achieved RMSE: **< 4000 (Proficient to Exemplary range on rubric)**

---

## How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/your-username/air-quality-forecasting.git
   cd air-quality-forecasting
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the notebook:

   ```bash
   jupyter notebook notebooks/air_quality_forecasting.ipynb
   ```

4. Generate predictions and create the submission file:

   ```bash
   python src/generate_submission.py
   ```

---

## Kaggle Submission

* File: `submission.csv`
* Format: exactly matches **sample\_submission.csv**
* Each row contains the predicted PM2.5 values for the test set

---

## References

* Kaggle Competition: *Air Quality Forecasting*
* Course Materials: *Machine Learning Techniques I*

---

**Author**: Armand Kay
**Course**: Machine Learning Techniques I
