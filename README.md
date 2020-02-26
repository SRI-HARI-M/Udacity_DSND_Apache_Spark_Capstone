# Sparkify

### Project overview
DSND Term 2 Capstone Project: A virtual company called 'Sparkify' offers paid and free listening service, the customers can switch between either service, and they can cancel their subscription at any time. The given customers dataset is huge (12GB).Thus the safest way to perform analysis is to use Big Data tools like Apache Spark which is one of the fastest big data tools.We worked with only a 128MB slice of the original dataset.

**The problem** is to create a machine learning model to predict the user intent to unsubscribe (Called customers' churn) before this happens.

### Files 
  - Sparkify.ipynb
  - Spark_Projects_Essentials.py
  - README.md

### Used resources
- Python 3.6.x (The programing language)
- pySpark 2.4.x (Machine learning library for big data)
- matplotlib 3.03 (A plotting library)
- pandas 0.23 (numerical calculations library)
- jupyter (The programming notebook interface)

## Git Repo

https://github.com/SRI-HARI-M/Udacity_DSND_Apache_Spark_Capstone

## Blogpost

https://sriharim2.blogspot.com/2020/02/a-blog-post-on-preventing-customer.html

### Generalization

**THIS GENERALIZATION IS TO MAKE SURE THAT THIS PROJECT CAN BE EASILY USED TO HOST THE MODEL IN ANY CLOUD PLATFORM.**

Through the file [`Spark_Projects_Essentials.py`] we can do the following:

Spark_Projects_Essentials.load_clean_transfer to read the data from the given source, clean the data, save the cleaned dataset to the new name as `new_dat_extraction.CSV`

Other Functions in Spark_Projects_Essentials.py: load_ml_dataset, get_train_test_features, apply_model

Loading data to `new_dat_extrac: tion.CSV` : ml_ds = load_ml_dataset(saved_as='new_dat_extraction.CSV')

Train, test portions for feature names : train, test, features_labels = get_train_test_features(ml_ds)

Create New Model:  apply_model(train, test, features_labels, model_name='GBT',save_as='NewGBT.model')

Load Existing Model: apply_model(train, test, features_labels,model_name='LR', load_from_existing='LogisticRegression.model')
