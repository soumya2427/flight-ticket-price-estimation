# flight-ticket-price-estimation
This project uses Python and Machine Learning to estimate the price of a flight ticket.
The README describes the project as follows:

Estimate flight ticket prices using airline, source, destination, travel month, booking lead time, stops, and duration.

Objectives
Explore flight booking data.
Analyze factors affecting ticket prices.
Compare different airlines and routes.
Clean and prepare the dataset.
Train a regression model.
Estimate the price of a new flight.
Technologies Used
Python
Pandas – data handling
NumPy – numerical operations
Matplotlib – graphs and visualization
Scikit-learn – machine learning
Machine Learning Algorithm

The project uses:

Linear Regression

Categorical data such as airline, source, destination and stops are converted using One-Hot Encoding, while numerical variables are standardized using StandardScaler.

3. Dataset Description

The CSV file contains 800 rows and 9 columns:

Column	Description
flight_id	Unique ID of each flight
airline	Airline operating the flight
source	Departure city
destination	Arrival city
travel_month	Month of travel, 1–12
days_before_booking	Number of days before the flight that the ticket was booked
stops	Number/type of stops
duration_hours	Flight duration in hours
ticket_price	Actual ticket price

There are some missing values in airline, destination, days_before_booking, stops and duration_hours. The Python program handles these automatically using imputation.

4. How the Python Program Works

The program follows this flow:

CSV Dataset
↓
Read data using Pandas
↓
Check missing values
↓
Separate input and target
↓
Preprocess numerical & categorical data
↓
Split into training and testing data
↓
Train Linear Regression model
↓
Predict ticket prices
↓
Evaluate model
↓
Predict price of a new flight
↓
Generate graphs

5. Input and Target Variables

The program removes:

flight_id

because it doesn't help predict the price.

The target is:

ticket_price

The model uses these inputs:

travel_month
days_before_booking
duration_hours
airline
source
destination
stops
6. Data Preprocessing
Numerical variables

The program processes:

Travel month
Days before booking
Duration

Missing numerical values are replaced with the median.

Then StandardScaler is used to scale the numerical values.

Categorical variables

The program processes:

Airline
Source
Destination
Stops

Missing categorical values are replaced with the most frequent value.

Then One-Hot Encoding converts categories into numerical values that the Linear Regression model can understand.

7. Model Training

The dataset is divided into:

80% training data
20% testing data

The model used is:

Linear Regression

The model learns the relationship between flight characteristics and ticket prices.

8. Model Performance

I ran the model from your file using the same settings.

The results are approximately:

Metric	Result
MAE	₹684.77
RMSE	₹859.20
R² Score	0.9279
Meaning

MAE = ₹684.77

On average, the model's prediction differs from the actual ticket price by around ₹685.

RMSE = ₹859.20

This measures prediction error while giving more weight to larger errors.

R² = 0.9279

This means the model explains approximately 92.8% of the variation in ticket prices in this dataset.

So, for this educational/synthetic dataset, the model performs quite well.
