# barossa-platform_service-machine_learning_account_mapping

Documentation of SageMaker Implementation of Mapping Algorithm for OneSource Statutory Reporting.

 

 

1) Initial Project

- The problem that we are trying to solve is that In the OSR application, users currently do manual data entry when categorizing data and files. Currently, it takes hours for users to manually put accounts into their respective categories. The team decided to add machine learning to solve this problem. We needed to create a mapping algorithm that is able to automate this process to make it easier for both the user and the OneSource Team. If the user wants to make changes to the way the data is categorized, the model will automatically learn to sort the accounts to user preference. This problem is not limited to just statutory reporting but rather can be generalized throughout the OneSource platform.

- Need to create a Natural Language Processing ML model that can do Text classification using AWS BlazingText within SageMaker and then use that model to create a mapping algorithm that can accurately predict/place where the accounts and categories need to go based on user preference

 

 

2) Account mapping

- From the templates, there are accounts being streamed in. Users create an excel sheet and then import that into statutory reporting.

- The magnitude of the project is millions of records across 20-30 thousand accounts.

- Within the wizard, there is the ability to map the external accounts to internal accounts

- However, this is all done manually so what we have to implement is creating an ML model that can accurately map the accounts to their correct spot

- Essentially you use the model to give the user mapped accounts and have them review it rather than manually map them so it makes it much less time-consuming.

- We also need to allow the ML model to learn when the user changes/reviews the mapped accounts. If the model incorrectly mapped something and the user changes it, the model should be able to catch its mistake next time.

 

 

3) Accounts categories/accounts assignment

- This feature allows for users to report on specific categories full of accounts rather than each account individually.

- Helps companies to report on bigger time periods like quarterly and annually

- Essentially the main idea for this section is that we need to map the accounts that have millions of records into categories.

- This is another version of “mapping” so what we need to create is an ML model that can correctly map whatever it's being used for rather than just specific things like accounts.

- This will make things much easier since the user can just review the categories and make sure its correct rather than tediously moving them to each spot. We need to train the model to make sure that it has high accuracy in the first place so there aren’t that many mistakes and when there are, the model will fix itself to make it correct.

 

 

 

 

What did we use for this Notebook Instance

 

  1) Python tools

   - Pandas

   - NumPy

   - MatplotLib

   - nltk

   - boto3

 

  2) How did we store the data

    -We used S3 Buckets to store the data -> a202990-mapping-osr-accounts-s3-bucket (S3 Bucket used)

 

  

 3) To rerun the training model, run the Jupyter Notebook from the beginning and then make sure to change

 4) For the future, to use the "ActualData.csv", the Notebook must be changed to be able to use pd.concat() and other Pandas methods to change the csv to a way that the model can understand. This has to be explored further.

 5) For automatic hyperparameter tuning, the ranges can be changed but note that it takes a longer or shorter time based on the range.

      - Note that currently the code will not run with changed hyperparemeter ranges of .05 to .15. This has to be explored further.
