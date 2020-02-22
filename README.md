## Welcome to Plagiarism-Detector using SageMaker

In this project, we will build a plagiarism detector that examines an answer text file and performs binary classification; labeling that file as either plagiarized or not, depending on how similar that text file is to a provided, source text. The source text files used in this project are slightly modified versions of a dataset created by Paul Clough (Information Studies) and Mark Stevenson (Computer Science), at the University of Sheffield. You can read all about the data collection and corpus, at their university webpage [here](https://ir.shef.ac.uk/cloughie/resources/plagiarism_corpus.html).

The goal of this project is to train a binary classification model using the extracted features via two techniques containment and longest common sequence of words. We hand picked few highly correlated containment features and used it to train and build a SVM model that was tested on few samples. We expect our model to classify a given answer text file as plagiarized or not plagiarized.
	
### Table of Contents

1. [Installation](#installation)
2. [Motivation](#motivation)
3. [Jupyter Notebook File (*.ipynb) Descriptions](#files)
4. [Summary Results](#summaryresults)
5. [Licensing, Authors, and Acknowledgements](#licensing)
	
## Installation <a name="installation"></a>

The python notebook file in this repo should run with Anaconda distribution of Python version 3.6.

To explore this project you can clone this repo via AWS SageMaker notebook instance and then work with **1_Data_Exploration.ipynb**, **2_Plagiarism_Feature_Engineering.ipynb** and **3_Training_a_Model.ipynb**. These notebooks have great documentation with a step by step walkthrough, simply guiding the user to build out a plagiarism detection model. 

This project was completed as part of Udacity's Machine Learning Nanodegree Certification.

## Motivation<a name="motivation"></a>

AWS provides quiet a number of cloud services for Data Scientists and Machine Learning Engineers to explore and learn concepts of Artificial Intelligence, Machine and Deep Learning. SageMaker provides easy to use options that helps create, validate and deploy Machine Learning models. In this project we built out a plagiarism detection model using the Jupyter notebook installation that is provided as part of AWS SageMaker. 

I think cloud technologies that vendors like AWS provide simply eases the way engineers can automatically build, test and deploy machine learning models into production enviroments. The SageMaker and other cloud services that AWS offers for machine learning provide a great motivation for eager data scientists.

## Files

The main files in this repo that are required for running of the web app are briefly summarized below (Please note that test case functions and other helper functions are imported from **helpers.py** and **problem_unittests.py**). You will need these files to successfully run the notebook files below.

1. **1_Data_Exploration.ipynb**
     - This notebook file provides a step by step walkthrough of the data exploration steps that was done prior to training our model. We looked at the breakdowns as bar plots showing the category counts of plagiarism levels for each task.
				
2. **2_Plagiarism_Feature_Engineering.ipynb**
     - This notebook file does the Feature Extraction steps and creates a training file train.csv to S3 bucket. We performed two techiniques i.e. Containment and Longest Common Sequence and finally extracted two important features we wanted to train our model with.  

3. **3_Training_a_Model.ipynb**
     - This notebook completes the model building and deploying steps of our project. We used sklearn Linear SVC classification model that performed well with our test files. 

## Summary Results

To summarize, I was able to successfully complete the tasks that were assigned to me in the notebooks mentioned above and finally create a sklearn LinearSVC model that was used to classify the provided answer files as plagiarized or not. In this case we used only few features and small set of text files to train and test our plagiarism model. The model actually performed well and produced 100% accuracy on the test files.

All analysis and results are well documented with the attached notebook files. Please review that for more details.

## Licensing, Authors, Acknowledgements

You can find the Licensing and other descriptive information about this project [here](https://github.com/kart-projects/Plagiarism-Detector/blob/master/LICENSE). Also, I should mention a special thanks to Udacity for having provided such a detailed notebook and documentation for this project. I only completed the sections in the notebook and scripts as part of assignment submission for Machine Learning Engineer Nanodegree Certification.
