# Radar data scripts

## Setup
Create a virtual environment: `pyhton3 -m venv .venv`.
If you are using visual studio code, it will detect that a new virtual environment is present and you can choose to use it.
Otherwise you can run `source .venv/bin/activate` to enter the virtual environment.

> **Virtual environment**: A folder in which you can install your project dependencies to isolate them from your regular work environment


## Run
To execute your software run:
```
radar_data_start
```

### Development
Just run `pip install -e .` and you are good to go!

#### Visual studio code
If you are using visual studio code install the recommended extensions



### Tools installed
- git, allows you keep track of your changes over time
- pre-commit, a software that runs some checks/scripts before you create a commit (like a "snapshot" of your code)
- ruff, a software that fixes your python code to make it pretty and readable, it gives you also hints on how to write modern and good python code
- detect-secrets, in order to prevent security leaks it will prevent you from committing secrets and passwords

#### What is an environment variable? and why should I use them?
Environment variables are variables that are not populated in your code but rather in the environment
that you are running your code. This is extremely useful mainly for two reasons:
- security, you can share your code without sharing your passwords/credentials
- portability, you can avoid using hard-coded values like file-system paths or folder names

you can place your environment variables in a file called `.env`, the `main.py` will read from it. Remember to:
- NEVER commit your `.env`
- Keep a `.env.example` file updated with the variables that the software expects

#### What is pyproject.toml?
`pyproject.toml` is a configuration file, in here you can define configurations for all the modern python devtools.
In `pyproject.toml` you can also specify your software dependencies, and even group them into different classes.
You can then use `pip` from your virtual environment to install them; this can be done with `pip install -e .` inside the root of the project.
This basically means: install this software as editable.
