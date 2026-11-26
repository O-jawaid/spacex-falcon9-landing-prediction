# SpaceX Falcon 9 First-Stage Landing Prediction
 
IBM Data Science Professional Certificate — Applied Data Science Capstone
 
## Table of Contents
- Project Overview
- Project Objectives
- Project Workflow
- Repository Structure
- Key Exploratory Findings
- Machine Learning Models & Results
- Model Evaluation & Conclusion
- Tools & Technologies
- Key Skills Demonstrated
- Final Deliverable
## Project Overview
 
SpaceX has significantly reduced the cost of space launches by recovering and reusing Falcon 9 rocket first stages. Historically, SpaceX advertised launch prices of approximately $62 million, compared with prices exceeding $165 million for some competing launch providers.
 
Predicting whether a Falcon 9 first stage will land successfully provides valuable insight into launch costs, mission planning, and the economics of reusable rockets.
 
This project uses historical SpaceX launch data to investigate the factors associated with first-stage landing success and develop machine learning models to predict recovery outcomes.
 
Completed as part of the IBM Data Science Professional Certificate, this capstone project demonstrates an end-to-end data science workflow, including data collection, web scraping, data wrangling, exploratory data analysis, interactive visualization, and predictive modeling.
 
## Project Objectives
 
The primary objectives of this project were to:
 
- Collect historical Falcon 9 launch data from publicly available sources.
- Clean, transform, and prepare launch data for analysis.
- Explore relationships between launch characteristics and first-stage landing outcomes.
- Investigate launch sites, payload characteristics, and mission profiles.
- Develop interactive geospatial visualizations and a data analytics dashboard.
- Build and evaluate machine learning classification models to predict landing success.
- Identify a suitable predictive model based on performance and interpretability.
## Project Workflow
 
The project was completed through the following stages:
 
- **Data Collection:** Retrieved historical launch records using the SpaceX REST API.
- **Web Scraping:** Extracted supplemental Falcon 9 launch information from Wikipedia using BeautifulSoup.
- **Data Wrangling:** Cleaned and transformed the collected data, handled missing values, and prepared the binary classification target variable.
- **Exploratory Data Analysis:** Investigated launch patterns, payload distributions, orbital destinations, and landing outcomes using SQL, Pandas, Matplotlib, and Seaborn.
- **Interactive Visualization:** Analyzed launch site locations using Folium and developed an interactive Plotly Dash dashboard to explore launch outcomes.
- **Machine Learning:** Trained, tuned, and evaluated four classification algorithms to predict Falcon 9 first-stage landing success.
**Dataset scope:** The SQL analysis uses a table of 101 launches through December 2020. The API-based machine learning dataset contains 90 Falcon 9 launches through November 2020, with booster landing outcomes. The interactive dashboard uses a separate, smaller launch file.
 
## Repository Structure
 
| File / Folder | Description |
|---|---|
| SpaceX_Capstone_Presentation.pdf | Final capstone presentation summarizing the methodology, findings, and model evaluation. |
| 01_spacex_api_data_collection.ipynb | Retrieves historical Falcon 9 launch records using the SpaceX REST API and filters out Falcon 1 launches. |
| 02_spacex_webscraping.ipynb | Extracts supplemental Falcon 9 launch information from Wikipedia using BeautifulSoup. |
| 03_spacex_data_wrangling.ipynb | Cleans the dataset, handles missing values, and prepares the binary target variable (Class: 1 = Success, 0 = Failure). |
| 04_eda_sql.ipynb | Uses SQL queries to investigate launch site activity, payload distributions, and booster performance. |
| 05_eda_dataviz.ipynb | Visualizes relationships between flight number, payload mass, orbit type, launch site, and landing success. |
| 06_launch_site_locations_folium.ipynb | Maps launch site locations and explores their proximity to coastlines, railways, highways, and populated areas. |
| spacex_dash_app.py | Interactive Plotly Dash application featuring launch site filtering and payload mass range selection. It loads a launch data CSV that is not included in this repository. |
| 07_spacex_machine_learning_prediction.ipynb | Preprocesses data, tunes hyperparameters, and evaluates four classification models. |
| images/ | Contains selected visualizations and screenshots from the analysis and dashboard. |
 
## Key Exploratory Findings
 
The exploratory data analysis revealed several patterns associated with Falcon 9 first-stage landing outcomes:
 
- **Landing Success Over Time:** Landing success generally improved as SpaceX gained operational experience and introduced newer booster configurations.
- **Launch Site Performance:** Launch sites exhibited differences in launch frequency and landing success rates. Kennedy Space Center LC-39A and Cape Canaveral Space Force Station SLC-40 were among the primary sites examined.
- **Payload Mass and Orbit:** Landing outcomes varied across payload mass ranges and orbital destinations, suggesting that mission characteristics are relevant when analyzing recovery success.
- **Geographic Analysis:** Folium visualizations provided insights into launch site locations and their proximity to coastlines and transportation infrastructure.
These findings helped identify relevant features and relationships for subsequent predictive modeling.
 
## Machine Learning Models & Results
 
Four supervised classification algorithms were developed to predict whether a Falcon 9 first stage would land successfully:
 
- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Decision Tree Classifier
### Model Development
 
The modeling workflow included:
 
- Preparing training and testing datasets using an 80/20 split.
- Applying feature scaling using StandardScaler.
- Performing hyperparameter optimization using GridSearchCV.
- Evaluating model performance using 10-fold cross-validation.
- Comparing cross-validation accuracy against test-set accuracy.
### Model Performance
 
| Model | Cross-Validation Accuracy | Test Accuracy |
|---|---|---|
| Logistic Regression | 84.64% | 83.33% |
| Support Vector Machine | 84.82% | 83.33% |
| K-Nearest Neighbors | 84.82% | 83.33% |
| Decision Tree | 89.11% | 66.67% |
 
## Model Evaluation & Conclusion
 
Logistic Regression, Support Vector Machine, and K-Nearest Neighbors achieved identical test accuracy of 83.33%, correctly classifying 15 out of 18 test observations.
 
Their cross-validation scores were also comparable, indicating similar predictive performance in this experiment.
 
The Decision Tree had the highest cross-validation accuracy (89.11%) but the lowest test accuracy (66.67%, 12 of 18 correct). This gap suggests it overfit the training data, so its cross-validation score was not a reliable guide to performance on unseen launches.
 
Logistic Regression was selected as the preferred model because it offered:
 
- Competitive predictive performance.
- Straightforward interpretability.
- Computational efficiency.
- A practical balance between predictive capability and model simplicity.
The relatively small test set limits the generalizability of the reported performance metrics. Therefore, the results should be interpreted with caution.
 
Nevertheless, this project demonstrates how historical launch data, exploratory analysis, and supervised machine learning can be combined to investigate and predict Falcon 9 first-stage landing outcomes.
 
## Tools & Technologies
 
| Category | Technologies |
|---|---|
| Programming Languages | Python, SQL |
| Data Collection | SpaceX REST API, Requests, BeautifulSoup |
| Data Manipulation | Pandas, NumPy |
| Database | SQLite |
| Data Visualization | Matplotlib, Seaborn, Plotly |
| Geospatial Visualization | Folium |
| Interactive Dashboards | Plotly Dash |
| Machine Learning | Scikit-Learn |
| Development Environment | Jupyter Notebook |
 
## Key Skills Demonstrated
 
This project demonstrates practical experience in:
 
- Data collection using REST APIs and web scraping.
- Data cleaning, preprocessing, and feature engineering.
- SQL querying and exploratory data analysis.
- Statistical analysis and data visualization.
- Geospatial analysis and interactive mapping.
- Interactive dashboard development using Plotly Dash.
- Supervised machine learning and classification.
- Feature scaling and hyperparameter optimization.
- Model evaluation and performance comparison.
- Communicating analytical findings through visualizations and presentations.
## Final Deliverable
 
IBM Applied Data Science Capstone Presentation
 
The final presentation summarizes the project objectives, data collection methods, exploratory findings, interactive visualizations, machine learning approach, and model evaluation results.
 
[View the SpaceX Capstone Presentation](SpaceX_Capstone_Presentation.pdf)
 
This project was completed as part of the IBM Data Science Professional Certificate Applied Data Science Capstone.
