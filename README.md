# Trend-Interview
This is the ML Model I built for the Trend interview on Monday, November 10th

# File Directory Structure

/Codebase/: Contains the entirety of the Machine Learning project including the environment setup, data handling, and model notebooks.

/Codebase/Environment/: Contains two environment files, one file called `tensorflow_env.yml` for the RNN model created in tensor.ipynb and the other environment file called `general_env.yml` is used for every other notebook.

/Codebase/Cleaning/: Contains two notebooks to clean and store the two datasets used for this interview project, please run these first before proceeding to the models.

/Codebase/Data/: Stores all of the data needed to run the model notebooks from, these must be first populated by the notebooks under the Cleaning directory.

/Codebase/Model-Development/: Contains the two directories for the models built from the two datasets, this will be extrapolated below.

/Codebase/Model-Development/Medical-Cost-Models/: Contains set of notebooks for each model used for regression models.

/Codebase/Model-Development/Specialty-Models/: Contains directory for the saved models as well as the set of notebooks for each NLP model used on this dataset such as the RNN under `tensor.ipynb` and the BERT models used under `bert.ipynb` as well as additional metric collection off of the saved models.

/Codebase/README.md: Contains [project information](Codebase/README.md) for how to setup one's environment and run the project, please proceed here to understand how set up the environment files for the project.