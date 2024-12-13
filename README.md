# ML-Assignment-Uber-Fare-Prediction

This project aims to predict Uber fares using historical ride data. By leveraging machine learning techniques, specifically the Random Forest Regressor, the goal is to accurately predict the fare of future Uber rides based on factors such as pickup and dropoff locations, passenger count, and time of day. This project can be used to gain insights into the factors affecting Uber fares and to optimize pricing strategies for Uber.

## Project Overview

The dataset used in this project contains various features such as:
- `key`: Unique identifier for each trip
- `fare_amount`: The cost of the trip in USD
- `pickup_datetime`: The date and time when the trip started
- `passenger_count`: The number of passengers in the ride
- `pickup_longitude` and `pickup_latitude`: Coordinates of the pickup location
- `dropoff_longitude` and `dropoff_latitude`: Coordinates of the dropoff location

## Steps Involved

1. **Data Preprocessing**
    - Data cleaning: Removing rows with missing or negative values
    - Feature engineering: Creating new datetime-related features (hour, weekday, etc.)
    - Outlier detection and removal for both fare amounts and geographical coordinates

2. **Exploratory Data Analysis (EDA)**
    - Distribution of fare amounts
    - Relationship between distance and fare
    - Impact of passenger count on fare
    - Geospatial analysis of pickup and dropoff locations

3. **Model Development**
    - Data split into training and testing sets
    - Random Forest Regressor was selected and trained on the dataset
    - Model evaluation using metrics like Mean Squared Error (MSE) and R² Score

4. **Model Results**
    - **MSE**: 22.02
    - **R² Score**: 0.78

## Libraries Used

- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Geopy
- Seaborn

## How to Run

1. Clone this repository to your local machine.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Run `uber_fare_prediction.py` to preprocess the data, train the model, and evaluate the performance.

## Results

- The Random Forest Regressor model provides accurate fare predictions with an R² of 0.78, meaning the model explains 78% of the variance in Uber fare prices.
- Distance and time-related features were found to be the most important predictors of fare amounts.

## Future Work

- Incorporating additional features such as traffic and weather data
- Exploring more advanced machine learning models such as Gradient Boosting or Neural Networks
- Real-time deployment for fare prediction

## License

This project is licensed under the MIT License - see the [LICENSE.txt](LICENSE.txt) file for details.
