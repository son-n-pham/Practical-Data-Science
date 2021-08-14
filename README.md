This is from the Practical Data Science specialization in Coursera provided by DeepLearning.AI and AWS

# INTRODUCTION TO PRACTICAL DATA SCIENCE

### Good overview of AI, Machine Learning, Deep Learning and Data Science from DeepLearning.AI

![overview](https://user-images.githubusercontent.com/79841341/128628651-1a245620-a219-43d9-b31d-fe3c80570902.png)

![MLInCloud](https://user-images.githubusercontent.com/79841341/128628702-6d8daf5e-bd7a-4ca8-a1e8-87be1462a88d.png)

### Machine Learning Workflow
![ML_Workflow](https://user-images.githubusercontent.com/79841341/128628732-85141321-4b72-4e4f-91d3-92ce50f50532.png)

### Popular Machine Learning Tasks
![ML_Tasks](https://user-images.githubusercontent.com/79841341/128628797-0a0e9394-efaf-488c-b204-269017b8d98f.png)

# WORKING WITH DATA

## Data Ingestion and Exploration

### Data Lakes
For ML, we first need to store lots of data into the place, which is centralized (Easy to access) and secure. The data storage needs to be suitable with all type of data including structured relational data (SQL), semi-structured data (JSON, html), unstructured data (images, video, audio files), streaming data. The data need to be governed, which means analysed, processed, analysed etc. That storage place is called data lake.

![data_lake](https://user-images.githubusercontent.com/79841341/128629012-8a859c7d-185a-4a82-bbcb-eadf5d81c88f.png)

### Amazon S3 is the data lake in AWS.
![image](https://user-images.githubusercontent.com/79841341/128629061-956fd499-5bf9-40ee-b1b2-7a835ef1dfc4.png)

### AWS Data Wrangler is the open-source Python tool for Amazon S3
- It is an open-source Python library
- Connects pandas and AWS data services
- Load/unload data from
  - data lakes
  - data warehouses
  - database

Example:
```Python
!pip install awswrangler

import awswrangler as wr
import pandas as pd

# Retrieving the data directly from Amazon S3
df = pd.s3.read_csv(path='s3://bucket/prefix/'
```
### AWS Glue Data Catalog is used to register data in Amazon S3
- Creates reference to data ("S3-to-table" mapping)
- Just metadata / schema stored in tables
- No data is moved
- *AWS Glue Crawler* can be set up to automatically
  - infer data schema
  - update data catalog

How-to register data

```Python
# First, import data wrangler
import awswrangler as wr

# Second, create a database in the AWS Glue Data Catalog
wr.catalog.create_database(
  name=...)

# Third, create CSV table (metadata only) in the AWS Glue Data Catalog
wr.catalog.create_csv_table(
  table=...,
  column_types=...,
  ...)
```

![AWS_Glue_Data_Catalog](https://user-images.githubusercontent.com/79841341/128629479-e64d2007-4005-44af-b810-2646acda915b.png)

### Now, we can query data in Amazon S3 with *Amazon Athena*

![Amazon_Athena](https://user-images.githubusercontent.com/79841341/128631337-bf890128-253c-4270-889a-6e69cb3a2911.png)

## Data Visualization 
![data_visualization](https://user-images.githubusercontent.com/79841341/128631859-35087fc7-f649-4299-9bc0-bbd9aaea51a0.png)

