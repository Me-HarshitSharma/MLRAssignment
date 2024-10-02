# Bike sharing service
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

# Problem statement 
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 


In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.


They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands


## Technologies Used
- numpy - version 2.1.1
- pandas - version 2.2.3
- matplotlib - version 3.4.3
- plotly - version 3.9.2
- seaborn - version 0.13.2
- statsmodels - version 0.14.3
- scikit-learn - version 1.5.2

## Dataset 
day.csv have the following fields:
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

## Features

The final model includes the following features after preprocessing:

- Season
- Year
- Holiday
- Weekday
- Weather Situation
- Feeling Temperature (atemp)
- Humidity
- Wind Speed

## Model Selection
- Linear regression was chosen because the linear relation between independent variables and the dependent variable was quite strong.

## Model Evaluation
- Assumptions of linear regression were validated using plots and residual analysis.
- Variance Inflation Factor (VIF) was used to check for multicollinearity among predictors.

## Results

- The final model achieved an R-squared value of `0.801`, indicating that approximately 80.1% of the variability in bike demand can be explained by the selected features.
- Key predictors include season, year, weather conditions, feeling temperature, and wind speed.
- The final model demonstrated a good fit, with a 0.78 R-squared value over the test dataset. The residual analysis and diagnostics indicated that the model met the assumptions of linear regression.

## Contact
Created by [@Me-HarshitSharma (https://github.com/Me-HarshitSharma)] - feel free to contact me!


## Dataset License

Use of this dataset in publications must be cited to the following publication:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}

Contact
For further information about this dataset please contact Hadi Fanaee-T (hadi.fanaee@fe.up.pt)
