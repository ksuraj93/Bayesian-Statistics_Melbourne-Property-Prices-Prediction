# Melbourne-Property-Prices-Prediction
## Analyse and Estimate the property prices in Melbourne by using Bayesian analysis in R

The dataset is a  fabricated dataset.  

#### The following are the parameters :

1. SalePrice: Sale price in AUD
2. Area: Land size in m2 of the sold property
3. Bedrooms: The number of bedrooms
4. Bathrooms: The number of bathrooms
5. CarParks: The number of car parks
6. PropertyType: The type of the property (0: House, 1: Unit)

The SalePrice is distributed as Normal(μ,σ2), where both of μ and σ2 are unknown. 
#### In the first section, we find the Bayesian estimate of mean sale price μ  in Melbourne and its variance σ2:

1. Create a model diagram for JAGS showing the distribution of sale prices and prior distributions of μ and σ2, considering domains of μ and σ2!
2. Specify non-informative prior distributions for both of μ and σ2.
3. Create JAGS data and model blocks based on the model diagram at the previous step.
4. Compile the model and create Markov chains using the compiled model.
5. Assess the appropriateness of the chains using the MCMC diagnostics.
6. Display the posterior distribution of mean sales price μ and its variance σ2.

#### In the second section, the sale prices in Melbourne is modelled using the other predictors given in the dataset. For each predictor, expert information and degree of belief in the prior information is given as follows:

1. Area: Every m2 increase in land size increases the sales price by 90 AUD. This is a very strong expert knowledge.
2. Bedrooms: Every additional bedroom increases the sales price by 100,000AUD. This is a weak expert knowledge.
3. Bathrooms: There is no expert knowledge on the number of bathrooms.
4. CarParks: Every additional car space increases the sales price by 120,000AUD. This is a strong expert knowledge.
5. PropertyType: If the property is a unit, the sale price will be 150,000 AUD less than that of a house on the average. 

#### In the final section, a Bayesian regression model is built to predict sale prices using the past sales information and expert knowledge:
1. Create a JAGS model diagram showing the multiple linear regression setting in this problem.
2. Specify the prior distributions reflecting the expert information for each predictor.
3. Create JAGS data and model blocks based on the model diagram and prior distributions at the previous steps.
4. Compile your model and create Markov chains using the compiled model.
5. Assess the appropriateness of the chains for each parameter using the MCMC diagnostics.
6. Display the posterior distribution of each parameter and draw inferences on Bayesian point and interval estimates.
7. Use the Bayesian point estimates of the model parameters to write the predictions model.
8. Find the predictions of sale prices for the properties given below:

PROPERTY | AREA | BEDROOMS | BATHROOMS | CARPARKS | PROPERTY TYPE
------------ | ------------- | ------------ | ------------ | ------------ | ------------
1 | 600 | 2 | 2 | 1 | UNIT
2 | 800 | 3 | 2 | 2 | HOUSE
3 | 1500 | 2 | 1 | 1 | HOUSE
4 | 2500 | 5 | 4 | 4 | HOUSE
5 | 250 | 3 | 2 | 1 | UNIT
