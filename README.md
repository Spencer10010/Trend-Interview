# Trend-Interview
This is the ML Model I built for the Trend interview on Monday, November 10th

# File Directory Structure
This subsection provides a high overview to the directories within this project and provide a quick grasp of where everything is located.

/Codebase/: Contains the entirety of the Machine Learning project including the environment setup, data handling, and model notebooks.

/Codebase/Environment/: Contains two environment files, one file called `rnn_env.yml` for the RNN model created in `rnn.ipynb` and the testing file `test_rnn.ipynb` and the other environment file called `general_env.yml` is used for every other notebook.

/Codebase/Cleaning/: Contains two notebooks to clean and store the two datasets used for this interview project, please run these first before proceeding to the models.

/Codebase/Data/: Stores all of the data needed to run the model notebooks from, these must be first populated by the notebooks under the Cleaning directory.

/Codebase/Model-Development/: Contains the two directories for the models built from the two datasets, this will be extrapolated below.

/Codebase/Model-Development/Medical-Cost-Models/: Directories for classification models and regression models, these save their best produced models within the Saved-Models directory.

/Codebase/Model-Development/Medical-Cost-Models/Data-Visualization: Directory hosting data visualization file that shows more context into the content of the dataset.

/Codebase/Model-Development/Medical-Cost-Models/Unsupervised-Learning: Hosts GMM and KMeans files to visualize how the data is clustered together for further insight.

/Codebase/Model-Development/Medical-Cost-Models/Classification: Contains classification models that will save their models in the Saved-Models directory

/Codebase/Model-Development/Medical-Cost-Models/Regression: Contains regression models that will save their models in the Saved-Models directory

/Codebase/Model-Development/Specialty-Models/: Contains directory for the saved models as well as the set of notebooks for each NLP model used on this dataset such as the RNN under `rnn.ipynb` and the BERT models used under `bert.ipynb` as well as additional metric collection off of the saved models.

/Codebase/README.md: Contains [project information](Codebase/README.md) for how to setup one's environment and run the project, please proceed here to understand how set up the environment files for the project.