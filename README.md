# RPI_Project

This is the code for the Biological Image Analysis project.


# Anaconda Environment Setup

## Overview
This document provides instructions on exporting an Anaconda environment and setting it up on another system.

## Exporting the Environment
To export your Anaconda environment, run the following command:

```bash
your_env_name="my_env"  # Replace with your environment name
conda env export --name $your_env_name > environment.yml
```

This will generate a file named `environment.yml`, containing all dependencies required for the environment.

## Setting Up the Environment on Another System
To recreate the environment on another system, follow these steps:

1. Install Anaconda or Miniconda if not already installed. You can download it from:
   - [Anaconda](https://www.anaconda.com/download)
   - [Miniconda](https://docs.conda.io/en/latest/miniconda.html)

2. Use the following command to create the environment from the exported `environment.yml` file:

   ```bash
   conda env create -f environment.yml
   ```

3. After the environment is created, activate it:

   ```bash
   conda activate my_env
   ```
   *(Replace `my_env` with the actual environment name specified in `environment.yml`.)*

## Verifying the Installation
To confirm that the environment has been set up correctly, check the installed packages:

```bash
conda list
```

If any issues arise, consider using the following troubleshooting steps:
- Ensure `environment.yml` is correctly formatted.
- Update Conda before running the installation:
  ```bash
  conda update -n base -c defaults conda
  ```
- If package conflicts occur, consider using `mamba` for a faster resolution:
  ```bash
  conda install -n base -c conda-forge mamba
  mamba env create -f environment.yml
  ```

## Additional Notes
- If you need to share a more compact environment, consider listing only explicit package versions:
  ```bash
  conda list --explicit > explicit-packages.txt
  ```
  Then, recreate the environment using:
  ```bash
  conda create --name my_env --file explicit-packages.txt
  ```
- To remove an environment, use:
  ```bash
  conda env remove --name my_env
  ```

For further assistance, refer to the [Conda Documentation](https://docs.conda.io/).

