# Sparkify User Churn Prediction
Udacity Data Scientist Nanodegree Capstone Project
 
Sparkify is a fictional music streaming platform created by Udacity. 
For this project we are given log data of this platform in order to drive insights and create a machine learning pipeline to predict churn. 

mini, medium and large datasets(only on AWS public) are available.
I have used medium scale data that I have processed with Spark on AWS EMR.

**Medium** : https://medium.com/@elifsurmelif/sparkify-user-churn-prediction-eff0868c5554

## Getting Started

Instructions below will help you setup your local machine to run the copy of this project.
You can run the notebook in local mode on a local computer as well as on a cluster of a cloud provider such as AWS or IBM Cloud.

### Prerequisites

#### Software and Data Requirements

  - Anaconda 3
  - Python 3.7.3
  
  - pyspark 2.4
  - pyspark.ml
  - pandas

Dataset:
  - mini_sparkify_event_data.json is the app data that you can play with. 
  - medium-sparkify-event-data.json.gz : this dataset is larger than github limits, it's gzipped.
  - If you have an AWS account, a large dataset(12 GB) has been public on s3n://udacity-dsnd/sparkify/sparkify_event_data.json

#### Running the notebooks

  - First install all the packages stated above.
  - Run the commands below in your working directory to open the project in jupyter lab:
    ```
    git clone https://github.com/elifinspace/sparkify.git
    
    jupyter lab
   
    ```
  - Sparkify_final_.ipynb : This notebook has all the functions for processing the data and ml pipeline.
  - sparkify_exploration_visuals.ipynb: This notebook has some sample visuals that have been generated during initial investigation. More detailed analysis could have been done to reveal relations and gain insights.
  
  If you have difficulty in displaying .ipynb files please go to  https://nbviewer.jupyter.org/ and paste the link that you're trying to display the notebook.
  And you can use http://htmlpreview.github.io/ to display html files.
## Metrics 
I have used f1score and AUC when evaluating the model.
It is important for us to be precise when labeling a customer as a churn. Because if we're giving away free products, we might be causing unnecessary cost if the user is not thinking of churn .or if we're sending messages regarding their reduced activity, this might get the user confused.

## Analysis and Discussion

The outputs are generated using medium sized dataset. This might have introduced a slight imbalance in the data.
It is also challenging to understand latent relations in the data.Feature selection is really important otherwise you might end up with a model with accuracy 1.0 but it is not true.
Moreover as a further work a common practice, A/B test can be considered.A set of actions can be determined to reduce churn and population can be split into control and experiment groups to validate the model and results.
More details can be found on Medium Blog Post: https://medium.com/@elifsurmelif/sparkify-user-churn-prediction-eff0868c5554

## Authors

* **Elif Surmeli**
