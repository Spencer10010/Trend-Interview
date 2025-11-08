# How to Setup Jupyter Notebook Environment

1. Create a conda environment from the .yml file provided in `/Environment` folder:
    - If you are running windows, use the Conda Prompt, on Mac or Linux you can just use the Terminal.
    - Use the command: `conda env create -f interview_env.yml`
    - This should create an environment named `interview_env`. 
2. Activate the conda environment:
    - Windows command: `activate interview_env` 
    - MacOS / Linux command: `conda activate interview_env`
3. Exit conda environment:
    - Use the command: 'conda deactivate'

If adding new dependencies use: 'conda env update --file interview_env.yml --prune' to update the environment.

For more references on conda environments, refer to [Conda Managing Environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) or the [Conda Cheat Sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)

# Where to Begin?

First generate the data locally using 'medical_cost_data_preprocessing.py' and 'specialty_data_preprocessing.py' in the `/Data` folder. Running the entirety of these notebooks will produce the datasets' CSVs within the `CSVs` directory.

Then use the model notebooks within to create respective models.