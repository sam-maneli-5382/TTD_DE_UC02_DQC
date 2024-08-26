# Data Engineer Assessment
## UC02: TTD_DE_UC02_DQC: Add Data Quality Checks to the Data Engineering Pipeline. Address Any Data Quality Issues

## Goal
As a data engineer, I want to setup quality checks to ensure that the data that is provided to business is of good quality and fit for use.

## Summary
It is important to ensure that the data provides meets the data quality standards setup by the organization and the data is fit for use.


* __Problem Statement__ - Business has experienced data with issues such as duplicates in the data or inconsistent data types than those reported by the source.

Business has asked the Data Engineering team to implement controls that ensure that the data is fit for use and detect any issues with the pipeline if this is not the case.

* __Description__ - Lately, business is reporting that the data provide by the sources have several issues. This has caused incorrect reports to be generated and poor customer experience. Business has lost trust in the data due to the poor data quality

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

## Code Complexity
- Low / Medium

## `Diagram - Also refer PDF in folder`


## Datasets:

`File Location`: Refer to the attached `data` folder for information

* Vehicles (vehicles.csv)  at the plants (plants.csv) are built to order (orders.csv) placed - order_number
* Customer (customers.csv) provides reviews(welcome_call.csv) 60 to 80 days after the vehicles are delivered(vin).
* Sales (sales_rep.csv) representatives are linked to dealership (dealers.csv) and have dealership names


## Expected Outcomes:

1. The Great Expectations framework must be used to perform the data quality checks.
2. Atleast 5 different types of checks must be implemented on each dataset.  Explaination of why the check would be appropriate for the datast must be provided.

### Libraries or Options used
* Jupyter Notebook - Install and run locally on your laptop or device.
* Great Expectations Framework (Note: Install if required)
* PySpark, Pandas and matplot lib or similar plotting libraries

## `Acceptance Criteria`

1. Only the Great Expectations framework can be used for this exercise.
2. Implement different types of checks on the three datasets (vehicles, customers, sales_rep) data and provide your findings.
3. Explain the checks you have implemented and how it would be useful in detecting Data quality issues to the business.  Refer to the current challenges that business has highlighted.
4. Explain how the framework would be useful when data is stored in an RDBMS such as MySQL. Illustrate the workflow using **draw.io** and export the output in pdf format.  Expected Output: draw.io diagram