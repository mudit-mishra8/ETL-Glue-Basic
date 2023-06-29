# Building AWS Glue Job using PySpark

![Project Image](https://drive.google.com/file/d/1QoHDUJlFZBOvTXkcxS5fK0R96aCn-sSc/view?usp=drive_link)

AWS Glue Jobs are used to build ETL (Extract, Transform, Load) jobs which extract data from sources, transform the data, and load it into targets. AWS Glue Jobs can be written in languages like Python and Scala. For this project, we will be using PySpark, which is the Python API for Apache Spark - a powerful open-source data processing engine. PySpark is especially useful when you need to handle large-scale data in an efficient manner.

In this project, we will be learning about setting up a data lake, creating a development environment for PySpark, and finally building an AWS Glue Job using PySpark.

## Introduction

We will start by creating a data lake with two datasets - 'sales' and 'customers'. AWS Glue Crawlers will be used to infer the schema of our data and create metadata tables in the AWS Glue Data Catalog.

Next, we will create an AWS Glue Development Endpoint which allows us to interactively develop and test our ETL code. Using a notebook attached to this development endpoint, we will practice fundamental operations such as loading data, merging two datasets into one, and writing the data back to Amazon S3.

In the development environment, you will practice fundamental operations such as loading the data, merging two datasets into one and writing data back to S3. We will merge the 'sales' and 'customers' datasets into a single dataset named 'CustomerSales' and write it back to S3.

Finally, we will create an AWS Glue Job with the code we developed in the notebook. This Glue Job automates the task of merging the datasets and can be scheduled or triggered based on specific conditions.


## Steps

1. **Set up Data Lake in Amazon S3**: Upload the 'sales' and 'customers' datasets to a bucket in Amazon S3.

2. **Create IAM Roles and Policies**: Ensure that AWS Glue has permissions to access Amazon S3 and other resources.

3. **Use AWS Glue Crawlers**: Create and run AWS Glue Crawlers to populate the AWS Glue Data Catalog with table definitions.

4. **Set up Development Endpoint**: Create an AWS Glue Development Endpoint and attach a notebook for interactive development.

5. **Develop and Test PySpark Code**: Write PySpark code in the notebook to load, transform, and store data.

6. **Create and Run AWS Glue Job**: Create an AWS Glue Job using the PySpark code and execute it.

Stay tuned for more details on each step!



## Step 1: Identify Relevant Data Sources

Identified and moved the files into S3 under specific folders.

- Service Used: **AWS S3**
- Action: Created an S3 bucket and folders.

![screenshot of s3 bucket creation](https://drive.google.com/file/d/1twmj5eDL1bHTh29PQ8Ul8Ny8YILOz8aa/view?usp=drive_link)
![screenshot 2 of s3 bucket creation](https://drive.google.com/file/d/1tok2MuMBFk71fW-rJPHPA9lMwukqbuM9/view?usp=drive_link)


## Step 2: Create IAM Role for AWS Glue

Created an IAM role that AWS Glue can assume for the necessary permissions.

- Service Used: **IAM**
- Action: Created an IAM role with policies for AWS Glue.

![screenshot of IAM role creation](https://drive.google.com/file/d/1lMe4UwRnE_tdhB0kYpT_TAlKrBwndCWG/view?usp=drive_link)

## Step 3: Create Database in AWS Lake Formation

Created a database and registered the Amazon S3 bucket as data lake storage.

- Service Used: **AWS Lake Formation**
- Action: Created a database and granted permissions.

![screenshot of database creation](https://drive.google.com/file/d/10nLHToaDoSqsdvYlT26vNvJJEz8fQuog/view?usp=drive_link)

## Step 4: Create Table by Running a Crawler

Used AWS Glue Crawlers to populate the AWS Glue Data Catalog with tables.

- Service Used: **AWS Glue**
- Action: Created a crawler to populate Data Catalog.

![screenshot of crawler creation](https://drive.google.com/file/d/1jJYNWdIa2ea0taCmn2U3_4PJ1Td7fN0w/view?usp=drive_link)
![screenshot of crawler creation](https://drive.google.com/file/d/11X-hcM0l2FfxSgazw8G_t4vNcLhld_vQ/view?usp=drive_link)

## Step 5: Grant Permissions to Data Catalog Tables

- Service Used: **AWS Lake Formation**
- Action: Granted permissions to IAM role for accessing the tables.

![screenshot of granting permissions](https://drive.google.com/file/d/1mII7F5fdDp_NF6ewesFt0EZEsrSpPG0k/view?usp=drive_link)

## Step 6: Develop PySpark Notebook for Data Transformation

Developed a PySpark Notebook to read data as Spark DataFrames, perform transformations, and write the result back to S3.

- Service Used: **AWS Glue Notebook**
- Action: Created a notebook and performed data transformation.

![screenshot of PySpark notebook](https://drive.google.com/file/d/1nTJi2Z5xbrR4BqgRqi7TRyHFe4mPNN8x/view?usp=drive_link)

## Step 7: Create and Execute Glue ETL Job

Created an AWS Glue Job using the script from the PySpark Notebook.

- Service Used: **AWS Glue**
- Action: Created and executed Glue ETL Job.

![screenshot of Glue ETL job](https://drive.google.com/file/d/1dQxK4tQvk4fk1eb1L6QR_Qv03noQBNCT/view?usp=drive_link)
![screenshot of Glue ETL job](https://drive.google.com/file/d/17rtALHaeDzY_xz4p6hJm87aRKvxTXFXZ/view?usp=drive_link)

## Conclusion

This project demonstrates how to efficiently perform ETL operations using AWS Glue, Lake Formation, and S3. It involves setting up the necessary permissions, using crawlers to populate the Glue Data Catalog, and writing PySpark scripts to transform the data.

## Future Enhancements

- We can have more tranformation if needed.
- Implement monitoring and logging for the Glue Job.

