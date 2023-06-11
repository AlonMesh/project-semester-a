# CarPriceEstimator
This repository contains code for building a car price prediction model. The project involves analyzing a dataset of cars, which includes tasks such as web scraping, data cleaning, splitting the data into training and testing sets, and exploring the data for insights. The primary objective of this project is to develop a predictive model that can accurately estimate the price of a car based on various factors and features.

## Introduction
This repository contains code for analyzing a dataset of cars. The dataset provides valuable insights into the characteristics and pricing of different cars. The analysis encompasses various stages, including web scraping to collect additional data, data cleaning to ensure data integrity, splitting the data for model training and evaluation, building a predictive model, and exploring the data for further insights.

## Web Scraping
The web scraping stage, performed in the `1.crawling.ipynb` Jupyter Notebook, involves retrieving additional data about cars from `carwiz.co.il`. The code uses the requests library to send HTTP requests and the BeautifulSoup library to parse the HTML content of web pages. By scraping relevant information, we enhance the dataset and potentially gain access to additional features or details about the cars.

## Data Cleaning
The data cleaning stage is crucial to ensure the integrity and quality of the dataset. The code performs various cleaning operations, such as handling missing values, removing duplicates, and standardizing data formats. These operations help create a clean and consistent dataset for further analysis and modeling.

## Splitting the Data
Splitting the data into training and testing sets is essential for model development and evaluation. The code divides the dataset into two subsets: one for training the predictive model and the other for evaluating its performance. This separation ensures that the model's accuracy and generalization can be properly assessed.

## Modeling
In this project, we explored several regression models to predict car prices. Below are the details and performance scores of each model:

### Dummy Model
As a baseline comparison, we trained a dummy model that predicts the average car price for all instances. This simple model serves as a benchmark for evaluating the performance of other models. The performance of the dummy model on the test set was as follows:

* RMSE: 0.0982 (~1%)
* R-squared score: -0.0001 (~0%)

The dummy model's RMSE score represents the average difference between the predicted car prices and the actual prices. The R-squared score indicates the proportion of the variance in the target variable that can be explained by the model. Since the dummy model predicts the same value for all instances, it performs poorly with an R-squared score close to zero.

### Linear Regression Model
We trained a Linear Regression model using the scaled training dataset. The model was evaluated using the Root Mean Squared Error (RMSE) metric. The performance of the Linear Regression model on the test set was as follows:

* RMSE: 0.0611 (6.1%)
* R-squared score: 0.8733 (87.3%)

### Decision Tree Regression Model
We also experimented with a Decision Tree Regression model using the scaled training dataset. The model was evaluated using the RMSE metric. The performance of the Decision Tree Regression model on the test set was as follows:

* RMSE: 0.3491 (34.9%)
* R-squared score: 0.7963 (79.6%)

### Test Set Performance
Finally, we evaluated the performance of the selected Linear Regression model on the previously unseen test set. The model achieved the following scores:

* RMSE: 0.06966 (69.6%)
* R-squared score: 0.8274 (82.7%)

Please note that the modeling process can be further refined and improved by exploring additional models, fine-tuning hyperparameters, and considering feature engineering techniques.

*Due to the constraints of our first semester course, we did not have the opportunity to explore and utilize more advanced models, such as neural networks and other sophisticated techniques. These models offer the potential for improved performance and enhanced predictive capabilities. However, as this is an introductory course, our focus was primarily on understanding fundamental concepts and building a strong foundation in regression analysis. We acknowledge that there are more advanced models available, but our current knowledge and skillset were limited to the models we utilized in this project.*

## Data Exploration
Data exploration plays a crucial role in understanding the dataset's characteristics, relationships between variables, and identifying patterns or trends. The code includes various visualizations, such as histograms and correlation analysis, to gain insights into the distribution of parameters and their impact on car prices.

## Requirements
To run the code in the Jupyter Notebooks, ensure you have the following libraries installed:

* numpy
* pandas
* requests
* beautifulsoup4
* matplotlib
* seaborn
* scikit-learn
You can install these libraries using pip or conda, depending on your Python environment.

## Usage
1. Clone this repository to your local machine or download the ZIP file.
2. Install the required libraries mentioned in the Requirements section.
3. Open the Jupyter Notebooks (`1.crawling.ipynb`, `2.dataCleaning.ipynb`, `3.splittingData.ipynb`, `4.modeling.ipynb`, `5.dataExploring.ipynb`) using Jupyter Notebook or Jupyter Lab.
4. Follow the instructions and run each notebook cell by cell to execute the code and progress through the analysis stages.
5. Ensure any required dataset files are present in the same directory as the notebooks.
Feel free to modify the code in the notebooks to adapt it to your specific needs and explore further analyses or visualizations.

## License
The code in this repository is licensed under the MIT License.

## Authors
This project was developed by Alon Meshulam and Aviya Oren, first-year students in the A semester of the "Introduction to Data Science" course.
