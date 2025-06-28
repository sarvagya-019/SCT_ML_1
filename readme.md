# House Price Prediction Model

This project predicts house prices using a linear regression model trained on a real estate dataset. The model uses only three features: **Square Footage**, **Number of Bedrooms**, and **Number of Bathrooms**. The workflow includes data preprocessing, feature scaling, model training, evaluation, and visualization of results.

## Features Used

- **Square_Footage**: Total area of the house in square feet.
- **Num_Bedrooms**: Number of bedrooms in the house.
- **Num_Bathrooms**: Number of bathrooms in the house.

## Workflow

1. **Data Loading**: The dataset is loaded from a CSV file.
2. **Preprocessing**: Only the selected features are used. Features are scaled using MinMaxScaler.
3. **Model Training**: A linear regression model from scikit-learn is trained on the data.
4. **Evaluation**: The model's predictions are binned into price ranges. Accuracy, precision, recall, and F1-score are calculated.
5. **Visualization**: The number of houses in each price range (actual vs predicted) is visualized using a bar chart.
6. **Prediction**: The model can predict prices for new houses based on the three features.

## How to Use

1. **Install requirements**  
   ```
   pip install numpy pandas matplotlib scikit-learn
   ```

2. **Run the Jupyter Notebook**  
   Open the notebook and run all cells in order.

3. **Test Predictions**  
   You can input new values for square footage, bedrooms, and bathrooms to predict house prices.

## Example Prediction

```python
new_data = pd.DataFrame({
    'Square_Footage': [1500],
    'Num_Bedrooms': [3],
    'Num_Bathrooms': [2]
})
new_data_scaled = scaler.transform(new_data)
predicted_price = model.predict(new_data_scaled)
print(f"Predicted House Price: {predicted_price[0]:.2f}")
```

## Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

## Visualization

A bar chart shows the number of houses in each price range for both actual and predicted values.

---

**Author:** Sarvagya Gupta  
**Dataset:** Provided in `house_price_regression_dataset.csv