# DSI-Project-2-Regression-Challenge-Ames-Housing-Data-

### Problem Statement

The main objective of this Data Science project - Regression Challenge is to predict the house prices in Ames Lowa.
According to many features provided by this dataset, we need to find the relationship between the sale price with other variables that will have effects to the sale price. Throughout the iterative modeling and features selection processes manually and function built-in (automatically), we will use the predictive modeling as a part of the assessment and evaluation process to gain a deeper insight from 80 variables which were directly related to the property sales

### Data Dictionary

| feature | dype |Description
| --- | --- | --- |
| MS SubClass | int64 |
| MS Zoning | object |Identifies the general zoning classification of the sale.
| Lot Frontage | float64 |Linear feet of street connected to property
| Lot Area | int64 |Lot size in square feet
| Street | object |Type of road access to property
| Lot Shape | object |General shape of property
| Land Contour | object |Flatness of the property
| Neighborhood | object |Physical locations within Ames city limits
| Condition 1 | object |Proximity to main road or railroad
| Condition 2 | object |Proximity to main road or railroad (if a second is present)
| Bldg Type | object |Type of dwelling
| House Style | object |Style of dwelling
| Overall Qual | int64 |Overall material and finish quality
| Overall Cond | int64 |Overall condition rating

10 Very Excellent
| Year Built | int64 |Original construction date
| Year Remod/Add | int64 |Remodel date (same as construction date if no remodeling or additions)
| Roof Style | object |Type of roof

Flat Flat
| Roof Matl | object |Roof material
| Exterior 1st | object |Exterior covering on house
| Exterior 2nd | object |Exterior covering on house (if more than one material)
| Mas Vnr Type | object |Masonry veneer type
| Mas Vnr Area | float64 |Masonry veneer area in square feet
| Exter Qual | object |Exterior material quality
| Exter Cond | object |Present condition of the material on the exterior
| Foundation | object |Type of foundation
| Bsmt Qual | object |Height of the basement
| Bsmt Cond | object |General condition of the basement
| Bsmt Exposure | object |Walkout or garden level basement walls
| BsmtFin Type 1 | object | Quality of basement finished area
| BsmtFin Type 2 | object |Quality of second finished area (if present)
| Total Bsmt SF | float64 |Total square feet of basement area
| Heating | object |Type of heating
| Heating QC | object |Heating quality and condition
| Central Air | object |Central air conditioning
| Electrical | object |Electrical system
| Gr Liv Area | int64 |Above grade (ground) living area square feet
| Bsmt Full Bath | float64 |Basement full bathrooms
| Bsmt Half Bath | float64 |Basement half bathrooms
| Full Bath | int64 |Full bathrooms above grade
| Half Bath | int64 |Half baths above grade
| Bedroom AbvGr | int64 |Number of bedrooms above basement level
| Kitchen AbvGr | int64 |Number of kitchens
| Kitchen Qual | object |Kitchen quality
| TotRms AbvGrd | int64 |Total rooms above grade (does not include bathrooms)
| Functional | object |Home functionality rating
| Fireplaces | int64 |Number of fireplaces
| Fireplace Qu | object |Fireplace quality
| Garage Type | object |Garage location
| Garage Yr Blt | float64 |Year garage was built
| Garage Finish | object |Interior finish of the garage Fin Finished
| Garage Cars | float64 |Size of garage in car capacity
| Garage Area | float64 |Size of garage in square feet
| Garage Qual | object |Garage quality
| Garage Cond | object |Garage condition
| Paved Drive | object |Paved driveway
| Wood Deck SF | int64 |Wood deck area in square feet
| Open Porch SF | int64 |Open porch area in square feet
| Enclosed Porch | int64 |Enclosed porch area in square feet
| 3Ssn Porch | int64 |Three season porch area in square feet
| Screen Porch | int64 |Screen porch area in square feet
| Pool Area | int64 |Pool area in square feet
| Mo Sold | int64 |Month Sold
| Yr Sold | int64 |Year Sold
| Sale Type | object |Type of sale
| SalePrice | int64 | the property's sale price in dollars


### Conclusion

My first Lasso score from cross validation before tuning is 93.38%, which means 93% of the variance in SalePrice can be explained by the model and also give a pretty good RMSE score. It means that on average the model will predict within $20,299.98 of the actual target. 

After tuning the model by removed some features that have an outsized negative impact on price, like an outlier. 
Now that the offending properties have been removed from the training data, I will split and scale the data again, and then fit a new lasso model to it. This new model should perform better than the original one. 

The model currently has an r2 score of .9138nd an RMSE of 22,420. Additional exploration of the data and feature engineering will likely improve the model’s performance, particularly with regards to high-value properties. 

As home values near $300,000 the model becomes less reliable. In the absence of this additional research, the model is currently ready for production on homes under $275,000.
