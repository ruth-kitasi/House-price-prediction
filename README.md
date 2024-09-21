# King County Housing Prediction Model
This project uses linear regression to forecast housing prices in King County, Washington. This project leverages a dataset containing various attributes of homes sold in the area, such as square footage, number of bedrooms and bathrooms, location, and other relevant features. By applying regression techniques, the model aims to provide accurate predictions that can assist homebuyers, sellers, and real estate professionals in making informed decisions.

**Authors**: 
- [@bouzart](https://github.com/bourzat)
- [@Ruthkitasi](https://github.com/Ruthkitasi)
- [@matjoee](https://github.com/matjoee)
- [@NicholasKIRUI](https://github.com/NicholasKIRUI)
- [@Robert-Kalafa](https://github.com/Robert-Kalafa)
- [@mayajbrio](https://github.com/mayajbrio)

## Business Problem
The unpredictability of house prices poses a significant challenge for various stakeholders, including potential homebuyers and real estate agents. These stakeholders require accurate and reliable house price predictions to make informed decisions. Homebuyers need to understand market trends to make prudent purchasing decisions while the  real estate agents need accurate data to advise their clients effectively.

## Objectives
Our role as data scientists is to develop a house price prediction model that meet the following objectives:-

1. Determine which features have the most significant impact on house prices.
2. Examine the correlations between different features and house prices to identify strong relationships.
3. Build a predictive model to estimate house prices based on features.

## Data 
The dataset used for this project includes housing sales data from King County, Washington, spanning the years 2014 to 2015. Each entry provides essential features of the houses sold, such as bedrooms, bathrooms, and living area size (sqft_living). The dataset also includes the sale price of each house, serving as the target variable for prediction.

## Methods
Following the CRISP-DM methodology, we cleaned and performed Exploratory Data Analysis (EDA) on our data, aiming to uncover key patterns and relationships. It provides insights into housing market trends in King County, Washington, from 2014-2015, highlighting influential factors like square footage, bedrooms, and bathrooms. It also employs linear regression to model the relationship between housing prices and key predictors from the KC Housing dataset. This statistical approach predicts prices based on features such as property size and amenities, aiding stakeholders in strategic decision-making.

## Results
Based on our EDA, we identified price, bathrooms, sqft_living ,grade, sqft_above, sqft_living15 as columns that have a linear relationship and the highest correlation to price indicating that an increase in these variables cause an increase in price. The figures below show the scatters plot between sqft_living and price as well as sqft_above and price showing a linear relationship between the two variables:

![scatterplot sqft_living and price](./images/scatter_plot1.png)

![scatterplot sqft_above and price](./images/scatter_plot2.png)

Taking a look at the correlation matrix below, the features selected for the model have a high correlation with the price.

![correlation matrix](./images/correlation_matrix.png)

Based on the above, we followed an iterative approach to modelling, starting with all the above variables and applying log transformations to the relevant numeric columns. The final linear regression model achieved an R-Squared of 0.61 indicating that our model explains 61% of the variability in houses prices.  

## Conclusions
In line with our objectives, we concluded on the following:

**1. Determine which features have the most significant impact on house prices.**
- Features such as sqft_living ,grade,  sqft_above, sqft_living15, bathrooms and sqft_base have the most significant impact on price due to ther positve correlation to price.

**2. Examine the correlations between different features and house prices to identify strong relationships.**
 - sqft_living shows the strongest positive correlation of  0.701917. this means that increase in sqft_living increases the price of the house.
 
**3. Build a predictive model to estimate house prices based on features.**
- The model has a moderate R² score, suggesting it captures some, but not all, of the variability in house prices.
- The MSE is relatively low compared to the variance of house prices, indicating credible model accuracy for our predictions.
- The consistent cross-validation MSE suggests the model's performance is stable across different subsets of data.

## Recommendations
Increasing the square footage of living space positively impacts the price of a house.Additionally, enhancing features that have a strong positive correlation with price can further boost property value. We recommend focusing on both expanding living space and improving key features to maximize the overall price of the house.

### Next Steps
- Gathering more data about the location of a house i.e, latitude and longitude can tell us which ammenities may be close to these houses that may influence their prices.
- The data is from 2014 to 2015, this may not be sufficient to generalize prices in the area as per this 2024 hence we may need to supplement our dataset.
- We need to look into other algorithms such as decision trees to boost the performance of our overall model.

## For More Information
See the full analysis in the [Juptyer Notebook](index.ipynb) or review this [presentation](./Phase_2_Project_Presentation.pdf)

## Repository Structure

```
├── data
├── images
├── notebooks
├── .gitignore
├──  Phase 2 Project Presentation.pdf
├── index.ipynb
├── README.md
```
