This folder looks to analyse a dataset of credit score ratings from a range of rating agenceis.
Analysis is split among several notebooks.

Start in the 'Import And Cleaning' notebook. This takes the dataset (Located in the Resources folder), 
	cleans the data, and loads it onto a Postgres database. Make sure to set your database credentials in config.py
This script does also create cleaned csvs of the data, if a postgres connection is unavailable.

The Raw Data Visualisation notebook generates some charts showing differences in rating from various agencies. 
The ComponentAnalysis uses TSNE to create a visualisation of groupings within the data.
The output charts from these notebooks can be found under the plots folder - there is no need to run them directly
The Optimized_Credit_rating_model notebook goes through the process of using a deep neural network
	to make a binary classifier for this dataset, identifying if a given set of financial data should get
	an A-calss rating (A, AA, or AAA) or not. This also uses a Keras optimiser to tune the hyperparameters of the model.

The Specific Classifier notebook attemps a similar classification, but for each individual credit rating
	rather than a simple binary classifier.

Sometimes there can be issues with cached models - deleting the keras_tuner_dir and rerunning a script 
	can often fix this.

Be sure to import all required libraries at the top of each notebook. An additional install of 'keras-tuner' may be required
	on top of this.