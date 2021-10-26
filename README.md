# Conda Poetry

This is a demonstration of how Conda and Poetry can be used in a Python project
for dev dependency management and production deployment.

## Requirements

- [conda or miniconda](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html)
- [Poetry](https://python-poetry.org/docs/master/#installation)

## How To Run this Demonstration

1. From this project directory, run `conda env create -f environment.yml`
1. Activate the environment: `conda activate condapoetry`
1. Run the app `uvicorn condapoetry.main:app --reload` and go to http://localhost:8000/

## How To Create a Conda/Poetry Environment

1. Create a conda environemnt: `conda create -n <env_name> python=3.8`
1. Activate the environemnt: `conda activate <env_name>`
2. Create a poetry project: `poetry new <project_dir>`
3. Add dependencies: `poetry add <pypi_packages>`
4. Export project dependencies to conda environment files:

   ```
   conda env export > environment.yml
   conda list --export > anaconda-deps.ana
   ```
   
   For an actual project, this step could be done with a pre-commit hook.

## Additional Info

https://www.anaconda.com/blog/using-pip-in-a-conda-environment
