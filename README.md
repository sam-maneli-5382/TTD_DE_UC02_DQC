# Data Engineer Assessment
## UC02: TTD_DE_UC02_DQC: Add Data Quality Checks to the Data Engineering Pipeline. Address Any Data Quality Issues

### Goal
As a data engineer, I want to setup quality checks to ensure that the data that is provided to business is of good quality and fit for use.

### Summary
It is important to ensure that the data provides meets the data quality standards setup by the organization and the data is fit for use.


* __Problem Statement__ - Business has experienced data with issues such as duplicates in the data or inconsistent data types than those reported by the source.

Business has asked the Data Engineering team to implement controls that ensure that the data is fit for use and detect any issues with the pipeline if this is not the case.

* __Description__ - Lately, business is reporting that the data provided by the sources have several issues. This has caused incorrect reports to be generated and poor customer experience. Business has lost trust in the data due to the poor data quality

* __Data Issues Reported__ : Business has documented and highlighted the following issues with the data over the last 3 months.

  a. Data source systems changing the schema of the data without informing business.
  b. Numerous duplicates in the sales_rep_master data in the data resulting in higher processing time and duplicates in the Semantic asset.
  c. Vehicle VIN number columns not having the right length of fields or missing data. VIN Length - 17 Characters
  d. Model Brand not in expected brand types - BMW, MINI, Rolls Royce or strings not matching the expectated format.
  e. Data is not updated during the weekly build due to the source system not having the data available.

* __Expected Outcome__ : Your manager has asked you to perform a Proof of Concept (PoC) of the Great Expectations Quality framework and demonstrate to the team the various features of the framework.

You need to evaluate the features and functionality of the [`Great Expectations Quality framework`](https://greatexpectations.io/).

1. The Framework must support integration with the AWS Platform and must be deployed on to AWS. The PoC demonstration must be done on your laptop locally.  

2. The Framework must perform Schema Validation (including data type validation), data validation for VIN number (Length:17) and not null columns (VIN numbers). Other checks that are deemed suitable can also be added.
3. The Framework must also detect if there are duplicates in the data.
4. Provide a compliance report of the data on a sample datasets.
5. Cost of the check is a concern for the IT department. Ensure that this is taken into account when implementing the checks.

### Code Complexity
- Low / Medium

### `Diagram - Also refer PDF in folder`

* [PDF file with Workflow - click here](https://github.com/bmwttd/TTD_DE_UC02_DQC/blob/main/TTD_DE_UC02_DQC.pdf)


### Sample Data for DQC
Sample data for the DQC is available on the Google Drive
* Download the data from Google Drive with link provided here [Google Drive](https://drive.google.com/file/d/1NBXP1nFhyuZGgO8YHLL6yQqAPuM1zNca/view?usp=sharing)
* Download the `data.zip` file from the google drive location and unzip the file on your desktop or within the google collab workspace.
* Data files are available in two format: You can use either the `*.csv` or the `*.json` files to complete the assignment. 

## Datasets:

`File Location`: Refer to the attached `data` folder for information. 
The `data` folder is at the following location. - [data.zip](
https://drive.google.com/file/d/1NBXP1nFhyuZGgO8YHLL6yQqAPuM1zNca/view?usp=sharing)

* Vehicles (vehicles.csv)  at the plants (plants.csv) are built to order (orders.csv) placed - order_number
* Customer (customers.csv) provides reviews(welcome_call.csv) 60 to 80 days after the vehicles are delivered(vin).
* Sales (sales_person.csv) representatives are linked to dealership (dealers.csv) and have dealership names
* Orders (orders.csv) - represents the orders that are placed by the customers.
* plants (plants.csv) - CSV files list of plants at which the vehicle is manufactured.
* Vehicle Make (vehicle_make.csv) - file containing the make, model and category of the vehicle.
* welcome_call (welcome_call.csv) - file containing user sentiment and feedback about the vehicle purchased. 


## Expected Outcomes:

1. The Great Expectations framework must be used to perform the data quality checks.
2. Atleast 5 different types of checks must be implemented on each dataset.  Explaination of why the check would be appropriate for the datast must be provided.

### Libraries or Options used
* Jupyter Notebook - Install and run locally on your laptop or device.
* Great Expectations Framework (Note: Install if required)
* PySpark, Pandas and matplot lib or similar plotting libraries

## `Acceptance Criteria`

1. Only the `Great Expectations` framework can be used for this exercise.
2. Implement different types of checks on the three datasets (vehicles, customers, sales_rep) data and provide your findings.
3. Explain the checks you have implemented and how it would be useful in detecting Data quality issues to the business.  Refer to the current challenges that business has highlighted.
4. Explain how the framework would be useful when data is stored in an RDBMS such as MySQL. Illustrate the workflow using **draw.io** and export the output in pdf format.  Expected Output: draw.io diagram


### Machine setup

1.	Google Collab access, if you have this then you can ignore the  next steps.
2.	Install python3, pandas, pyspark and jupyterlab for notebooks

### Submission instructions
Please follow the below steps to commit your changes to the GitHub repository:
1.	If you do not already have a github account, kindly create one on https://github.com/.  
2.	Login to your github.com account. 
3.  Fork this repository to your own username profile and make the repository visibility `private`.  Ensure that your repository is `private`. Need help making the repo [private - refer here](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/setting-repository-visibility#making-a-repository-private)
5.  The repository name should be as below depending on the challenge you intend to solve.   
   - 	`TTD_DE_UC01_EDA`  - Exploratory Data Analysis
   - 	`TTD_DE_UC02_DQC` – Data Quality Checks.  
6. Add a .gitignore file to exclude the “*.csv / *.json and any other data files”. Do not include any data files. 
7. Ensure that all the supporting artifacts such as diagrams, code files, custom python packages developed by you etc are included in your repository. 
8. Commit all your changes to the “main” branch locally and push the changes to the github.com repository you created above.  
9. Add username: “bmwttd”as a contributor on your repository with both read/write access to your repository.  Please note you will fail the assessment if we cannot read your repository.
10. Email your TES with your name and link to your repository or follow the instructions provided by your TES for submission. 
