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

