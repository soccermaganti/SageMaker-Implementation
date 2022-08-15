

Documentation of SageMaker Implementation of Mapping Algorithm for Statutory Reporting.

 

 

1) Initial Project

- The problem that we are trying to solve is that In the company application, users currently do manual data entry when categorizing data and files. Currently, it takes hours for users to manually put accounts into their respective categories. The team decided to add machine learning to solve this problem. We needed to create a mapping algorithm that is able to automate this process to make it easier for both the user and the operations Team. If the user wants to make changes to the way the data is categorized, the model will automatically learn to sort the accounts to user preference. 

- Need to create a Natural Language Processing ML model that can do Text classification using AWS BlazingText within SageMaker and then use that model to create a mapping algorithm that can accurately predict/place where the accounts and categories need to go based on user preference




What did we use for this Notebook Instance

 

  1) Python tools

   - Pandas

   - NumPy

   - MatplotLib

   - nltk

   - boto3

 

  2) How did we store the data

    - We used S3 Buckets to store the data -> a202990-mapping-osr-accounts-s3-bucket (S3 Bucket used)

 

  

 3) To rerun the training model, run the Jupyter Notebook from the beginning and then make sure to change

 4) For the future, to use the "ActualData.csv", the Notebook must be changed to be able to use pd.concat() and other Pandas methods to change the csv to a way that the model can understand. This has to be explored further.

 5) For automatic hyperparameter tuning, the ranges can be changed but note that it takes a longer or shorter time based on the range.

      - Note that currently the code will not run with changed hyperparemeter ranges of .05 to .15. This has to be explored further.
