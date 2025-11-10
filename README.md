# Trend Health Partners Interview Project
This is the ML Model I built for the Trend interview on Monday, November 10th.

I produced an in depth discussion about my project, the processes and decisions I made, along with the general results I achieved on this [website](https://spencer10010.github.io/Trend-Interview/index). For a more in depth commentary and description, please proceed there.

If you would like to view the content of the website locally, feel free to look at the [homepage](docs/index.md), [traditoinal models](docs/classification_and_regression.md), and [text processing models](docs/bert_and_rnn.md) to gain further insight into the order of operations to take for each segment of the project.

# File Directory Structure
This subsection provides a high overview to the directories within this project and provide a quick grasp of where everything is located.

All of the code is within the Codebase directory, please proceed to that directory and read the README file within to learn how to setup your environment to work on the project.

/Codebase/: Contains the entirety of the Machine Learning project including the environment setup, data handling, and model notebooks.

/Codebase/README.md: Contains [project information](Codebase/README.md) for how to setup one's environment and run the project, please proceed here to understand how set up the environment files for the project.

/Codebase/Environment/: Contains two environment files, one file called `rnn_env.yml` for the RNN model created in `rnn.ipynb` and the testing file `test_rnn.ipynb` and the other environment file called `general_env.yml` is used for every other notebook.

/Codebase/Cleaning/: Contains two notebooks to retrieve, clean, and store the two datasets used for this interview project. Please run these files first before proceeding to creating the models.

/Codebase/Data/: Stores all of the data required to train the models from, these must be first populated by running the notebooks within the Cleaning directory.

/Codebase/Model-Development/: Contains the two directories for the models built from the two datasets, both directories will be extrapolated further below.

/Codebase/Model-Development/Medical-Cost-Models/: Contains directories for classification models and regression models, these save their best produced models within the Saved-Models directory. There are additional files within to interpret the code further and perform unsupervised learning upon the datasets.

/Codebase/Model-Development/Medical-Cost-Models/Data-Visualization: Directory containing the data visualization file that can provide more context into the dataset.

/Codebase/Model-Development/Medical-Cost-Models/Unsupervised-Learning: Hosts files files for GMM and KMeans to visualize how the data is clustered together for further insight.

/Codebase/Model-Development/Medical-Cost-Models/Classification: Contains classification models that will save their models in the Saved-Models directory.

/Codebase/Model-Development/Medical-Cost-Models/Regression: Contains regression models that will save their models in the Saved-Models directory.

/Codebase/Model-Development/Specialty-Models/: Contains directory for the saved models as well as the set of notebooks for each NLP model used on this dataset such as the RNN under `rnn.ipynb` and the BERT models used under `bert.ipynb` as well as additional metric collection off of the saved models.

/docs: This directory contains everything required to build the GitHub pages locally and within the GitHub actions interface.