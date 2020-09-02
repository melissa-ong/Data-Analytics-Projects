# ToyotaCorolla-Project

## Project Overview 

In this project, I complete a data analysis process, beginning with posing an objective of the analysis, and ending with reporting my findings and conclusions. 


## Project Table of Contents: 
* Objective
* Data Set
* Column Descriptions
* Accessing the Data
* Cleaning the Data
* Analyzing and Visualizing the Data 
* Model Evaluation and Validation
* Findings and Conclusions


### Objective

Develop a model for predicting the price of a Toyota Corolla for sale. Determine what factors influence the price. 


### Data Set

The dataset contains 37 specifications of 1436 used Toyota Corolla cars for sale, including price, and was downloaded from Kaggle. 

### Column Descriptions:

* **ID:** ID number
* **Model:** Car model
* **Price:** Offer price in Euros
* **Age:** Age in months
* **Mfg_Month:** Manufacturing month (1-12)
* **Mfg_Year:** Manufacturing year
* **KM:** Accumulated kilometers on odometer
* **Fuel_Type:** Fuel Type (Petrol, Diesel, CNG)
* **HP:** Horsepower
* **Met_Color:** Metallic Color? (Yes=1, No=0)
* **Automatic:** Automatic? (Yes=1, No=0)
* **cc:** Cylinder Volume in cubic centimeters
* **Doors:** Number of doors
* **Cylinders:** Number of cylinders
* **Gears:** Number of gear positions
* **Quarterly_Tax:** Quarterly road tax in Euros
* **Weight:** Weight in Kilograms
* **Mfr_Guarantee:** Within manufacturer’s guarantee period (Yes=1, No=0)
* **BOVAG_Guarantee:** BOVAG (Dutch dealer network) guarantee (Yes=1, No=0)
* **Guartantee_Period:** Guarantee period in months
* **ABS:** Anti-lock brake system (Yes=1, No=0)
* **Airbag_1:** Driver airbag (Yes=1, No=0)
* **Airbag_2:** Passenger airbag (Yes=1, No=0)
* **Airco:** Airconditioning (Yes=1, No=0)
* **Automatic_airco:** Automatic airconditioning (Yes=1, No=0)
* **Boardcomputer:** Boardcomputer (Yes=1, No=0)
* **CD_Player:** CD player (Yes=1, No=0)
* **Central_Lock:** Central lock (Yes=1, No=0)
* **Powered_Windows:** Powered Windows (Yes=1, No=0)
* **Power_Steering:** Power Steering (Yes=1, No=0)
* **Radio:** Radio (Yes=1, No=0)
* **Mistlamps:** Mistlamps (Yes=1, No=0)
* **Sport_Model:** Sport model (Yes=1, No=0)
* **Backseat_Divider:** Backseat Divider (Yes=1, No=0)
* **Metallic_Rim:** Metallic Rim (Yes=1, No=0)
* **Radio_cassette:** Radio Cassette (Yes=1, No=0)
* **Tow_Bar:** Tow Bar (Yes=1, No=0)


### Accessing the Data

Downloaded the csv file from Kaggle. I began by importing the data into a Jupyter notebook and exploring the data by checking the data types. This allowed me to determine that two of the variables (Model ID and Fuel_type) contain text strings, while all other variables were integer numbers. 

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
