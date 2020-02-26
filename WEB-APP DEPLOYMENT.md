# Sparkify


### Generalization

**THIS GENERALIZATION IS TO MAKE SURE THAT THIS PROJECT CAN BE EASILY USED TO HOST THE MODEL IN ANY CLOUD PLATFORM.**

Through the file [`Spark_Projects_Essentials.py`] we can do the following:

Spark_Projects_Essentials.load_clean_transfer to read the data from the given source, clean the data, save the cleaned dataset to the new name as `new_dat_extraction.CSV`

Other Functions in Spark_Projects_Essentials.py: load_ml_dataset, get_train_test_features, apply_model

Loading data to `new_dat_extrac: tion.CSV` : ml_ds = load_ml_dataset(saved_as='new_dat_extraction.CSV')

Train, test portions for feature names : train, test, features_labels = get_train_test_features(ml_ds)

Create New Model:  apply_model(train, test, features_labels, model_name='GBT',save_as='NewGBT.model')

Load Existing Model: apply_model(train, test, features_labels,model_name='LR', load_from_existing='LogisticRegression.model')



### Deployment as a Web Application

**THIS	IS TO EXPLAIN HOW THE MODEL CAN BE POTENTIALLY USED IN A WEB APPLICATION.**

- Using the file [`Spark_Projects_Essentials.py`], separate .py scripts should be created for each function as needed.

- Backend: JAVA

- FRONT-END: Javascript, HTML, Angular, Ajax

- DATA: JSON ['mini_sparkify_event_data.json']['new_data.json']

- The JAVA program is used to write POJO(Plain Old Java Object) and specifice SPARK package classes in order to call the necessaty .py scripts to perform actions on the data and display output