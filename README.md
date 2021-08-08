# Practical-Data-Science
This is from the Practical Data Science specialization in Coursera provided by DeepLearning.AI and AWS

Good overview of AI, Machine Learning, Deep Learning and Data Science from DeepLearning.AI

![overview](https://user-images.githubusercontent.com/79841341/128628651-1a245620-a219-43d9-b31d-fe3c80570902.png)

![MLInCloud](https://user-images.githubusercontent.com/79841341/128628702-6d8daf5e-bd7a-4ca8-a1e8-87be1462a88d.png)

Machine Learning Workflow
![ML_Workflow](https://user-images.githubusercontent.com/79841341/128628732-85141321-4b72-4e4f-91d3-92ce50f50532.png)

Popular Machine Learning Tasks
![ML_Tasks](https://user-images.githubusercontent.com/79841341/128628797-0a0e9394-efaf-488c-b204-269017b8d98f.png)

For ML, we first need to store lots of data into the place, which is centralized (Easy to access), secure. The data storage needs to be suitable with all type of data including structured relational data (SQL), semi-structured data (JSON, html), unstructured data (images, video, audio files), streaming data. The data need to be governed, which means analysed, processed, analysed etc. That storage place is called data lake.
![data_lake](https://user-images.githubusercontent.com/79841341/128629012-8a859c7d-185a-4a82-bbcb-eadf5d81c88f.png)

Amazon S3 is the data lake in AWS.
![image](https://user-images.githubusercontent.com/79841341/128629061-956fd499-5bf9-40ee-b1b2-7a835ef1dfc4.png)

AWS Data Wrangler is the open-source tool in Aamazon S3, which is connecting pandas with AWS data services.
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
