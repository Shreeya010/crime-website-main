1. Project Structure:
• app.py: Main Flask application file
• routes.py: Contains all the route handlers
• prediction.py: Handles crime prediction logic
• webscapper.py: Web scraping functionality
• templates/: Contains HTML templates
• static/: Contains static files (CSS, JS, images)
• actualdata2.csv: Dataset for crime analysis
***how this crime analysis website works in detail:***
1. Application Setup (app.py):
• This is a Flask web application
• Uses Flask-Compress for compression
• Has Google Sheets API integration (currently commented out)
• Configures various app settings like template auto-reload and compression
2. Routes (routes.py):
The website has several main pages:
• / or /index: Homepage
• /crime-charts: Displays crime statistics and charts
• /crime-locator: Shows crime locations on a map
• /crime-predictor: Allows users to predict future crime rates
• /feed: News feed related to crimes
• /predict: API endpoint for making crime predictions
3. Prediction System (prediction.py):
Two main prediction functions:
• predict_crime(state, year, crime_type):
• Uses Linear Regression for predictions
• Takes state, year, and crime type as inputs
• Uses historical data from actualdata2.csv
• Encodes state names using LabelEncoder
• Returns predicted crime numbers
• predictfun():
• Uses Facebook Prophet for time series forecasting
• Makes predictions for 365 days into the future
• Generates visualization plots
• Saves predictions as JSON files
4. Data Flow:
• Historical crime data is stored in actualdata2.csv
• Web scraping functionality in webscapper.py can update this data
• Predictions are made using both linear regression and time series analysis
• Results are displayed through various visualizations
5. Key Features:
• Crime prediction based on state and year
• Time series forecasting for future trends
• Interactive charts and visualizations
• Error handling for both 404 and 500 errors
• File upload capability for new data
6. Important Technical Details:
• Uses machine learning (Linear Regression and Prophet)
• Handles both GET and POST requests
• Implements error handling
• Uses JSON for data exchange
• Supports file uploads
• Generates and saves visualizations
7. External Dependencies (from requirements.txt):
• Flask for web framework
• Pandas for data manipulation
• Scikit-learn for machine learning
• Prophet for time series forecasting
• Various other supporting libraries
8. Security Considerations:
• Error handling for invalid inputs
• File upload validation
• JSON response validation
• Secure route handling
9. Deployment:
• Has a Procfile for deployment
• Configurable port settings
• Debug mode settings
• Static file serving configuration

***This is a comprehensive crime analysis system that combines web development, data science, and
machine learning to provide crime predictions and analysis. The modular design allows for easy
maintenance and future enhancements.***
