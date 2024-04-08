# Personal_Loan_Modelling

## Description 
This is a Personal Loan Modelling using Support Vector Machine (SVM) method. This predictive technique will forecast whether individual customers accept the personal loan offer or not. This greatly improves the efficiency of marketing campaign as it classifies those are more possible to accpet the offer and so the organisation will likely to promote their loan service successfully by pivoting on target customers.

## Analytics Background
Capitalising on machine learning for loan prediction brings 3 main advantages for finanacial insititutions:

1. **Risk assessment precision:**
   - Analyse historical data and applicant features to predict loan default risk accurately.
   - Minimise losses by identifying low-risk applicants likely to accept loan offers.

2. **Targeted marketing optimisation:**
   - Tailor marketing strategies based on customer characteristics and behavioral preferences.
   - Enhance lead conversion rates by focusing efforts on qualified loan applicants.

3. **Resource allocation efficiency:**
   - Prioritise leads with high likelihood of conversion to optimise resource use.
   - Increase operational efficiency and reduce costs in sales and marketing efforts.

## Data Input and Preparation

### Feature names
| Age | Experience | Income | Zip code | Family | CCAvg | Education | Mortgage | Personal_loan | Security_account | Cd_account | Online | Creditcard |
|-----|------------|--------|----------|--------|-------|-----------|----------|---------------|------------------|------------|--------|------------|

### Data cleansing
Highlighting two essential data preparation steps for modelling out of the 13 features:

* Converting negative values in the 'Experience' column to positive using the 'Absolute Conversion' method to address data entry errors.
* Transforming 'ZIP Code' into 'Place', 'Latitude', and 'Longitude' to quantify location input for predictive modeling accuracy.

#### Note: You can find the dataset and feature explanations stored in the Data_source folder.
