# How to Setup Jupyter Notebook Environment

1. Create a conda environment from the .yml files provided in `/Environment` folder:
    - If you are running Windows, use the Conda Prompt, on Mac or Linux you can just use the Terminal.
    - Use the command: `conda env create -f general_env.yml` and `conda env create -f rnn_env.yml`
    - This should create two environments named `general_env` and `rnn_env`. 
2. Activate the conda environment:
    - You should activate the environment for general_env to work with every notebook except for rnn.ipynb which for this notebook the environment rnn_env should be used. Replace NAME with general or rnn based on relevant needs.
    - Windows command: `activate NAME_env` 
    - MacOS / Linux command: `conda activate NAME_env`
3. Exit conda environment:
    - Use the command: 'conda deactivate'

If adding new dependencies use: 'conda env update --file general_env.yml --prune' to update the general environment and 'conda env update --file rnn_env.yml --prune' to update the rnn environment.

For more references on conda environments, refer to [Conda Managing Environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) or the [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

# Where to Begin?

First generate the data locally using 'medical_cost_data_preprocessing.py' and 'specialty_data_preprocessing.py' in the `/Data` folder. Running the entirety of these notebooks will produce the datasets' CSVs within the `CSVs` directory.

Then use the model notebooks within to create respective models of interest.