#  What Drives the Price of a Used Car?

## Overview and Data
We will explore a dataset from [Kaggle](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data). 
The original dataset contained information on 3 million used cars. 
The provided dataset contains information on 426K cars to ensure speed of processing. 
Our goal is to understand what factors make a car more or less expensive. 
As a result of our analysis, we will provide clear recommendations to our client -- a used car dealership -- as to what consumers value in a used car.

To frame the task, we will refer back to a standard process in industry for data projects called CRISP-DM. 
This process provides a framework for working through a data problem. 


## Deliverables
After understanding, preparing, and modeling our data, we write up a basic report that details our primary findings. 
The audience for this report is a group of used car dealers interested in fine-tuning their inventory.


## Data Description
From [Kaggle](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data), we get a description of the available features. 
The data is collected from Craigslist and contains:

- id: entry ID
- region: craigslist region
- price: entry price
- year: entry year
- manufacturer: manufacturer of vehicle
- model: model of vehicle
- condition: condition of vehicle
- cylinders: number of cylinders
- fuel: fuel type
- odometer: miles traveled by vehicle
- title_status: title status of vehicle
- transmission: transmission of vehicle
- VIN: vehicle identification number
- drive: type of drive
- size: size of vehicle
- type: generic type of vehicle
- paint_color: color of vehicle
- state: state of listing


   
## Summary of Findings
- By far the most important feature to predict the price is the car's **entry year**.
There is a moderate to strong positive correlation between the price and year: The newer the car, the higher its price.

- The second most important feature to predict the price is the car's **odometer**, which also stands out from the remaining features.
There is a moderate negative correlation between the price and odometer: The more the car has travelled, the lower its price.

- The group of third most important features are the car's **manufacturer**, **type of drive**, **generic type**, and **number of cylinders**, which are all of similar importance:
    - Porsche, RAM, and Jaguar are the most expensive manufacturers. The second-most expensive manufacturers are Audi, Rover, and GMC. Chrysler is the least expensive manufacturer, followed by Hyundai, Fiat, KIA, Honda, Nizzan, and Mazda.
    - Cars with front wheel drive are cheaper than cars with rear wheel drive or 4 wheel drive.
    - Mini-vans are the cheapest car type. Pickups and not listed types are the most expensive, followed by trucks.
    - Cars with 8 cylinders are generally more expensive than cars with 6 or 10 cylinders, and the latter are generally more expensive than cars with 4 cylinders.
    
- The fourth most important feature to predict the price is the car's **fuel type**. Gas and hybrid cars are cheaper than other fuel types.

These were the most important features to predict the car's price.
<br><br>

Features of less importance are:

- The car's condition: Cars in good to new conditions are more expensive than cars in salvage or fair conditions. The majority of used cars out for sale are in good or excellent conditions.
    
- The car's location (state) and color is the group of second least important features:
    - On average, cars in the states VA, CT, PA, NJ, OH, MI, and DC are the least expensive, while cars in the state MT are the most expensive. Otherwise, there is not so much significant difference among the states.
    - The lower relevance of color is what we would expect. Though, white and black cars seem to be the most expensive ones, while purple or green cars seem to be the cheapest ones.

- The car's transmission and size are the least important features, which makes sense:
    - 83% of the transmission data is either automatic or manual, and both categories have similar price statistics.
    - The three size categories are also very similar in their price statistics.

## Link to Notebook

[used_car_prices.ipynb](https://github.com/jessi88/used_car_prices/blob/main/used_car_prices.ipynb)
