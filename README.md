# Josep Suggestions   

.. image:: https://www.repostatus.org/badges/latest/wip.svg
   :alt: Project Status: WIP – Initial development is in progress, but there has not yet been a stable, usable release suitable for the public.
   :target: https://www.repostatus.org/#wip

The aim of this repo is to create an app to visualise and analyse the best cuisine recommendations from Josep's list. 🍲 
This project is developed using Python + R. 


# 1. How to use enviroment 

## renv 

We use `renv` to set-up the development environment for the project. Check more of `revn` in its full documentation [here](!https://rstudio.github.io/renv/articles/renv.html). 

Follow the next steps to set-up the environment: 


**1. Installation**

The following lines will install the renv package. This only needs to be run once! 

```R

if (!requireNamespace("remotes"))
  install.packages("remotes")

remotes::install_github("rstudio/renv")
```

**2. Initilise the environment**

renv creates a file called `renv.lock` that contains all packages needed in this project. Initialise means to install those packages with the specified version. This only needs to be run when you start working form 0 or when you want to restore your environment. 

```R
renv::init()
```

**3. Working** 

Once you have installed your packages, you can start working on the project. You can install new packages but they will not affect the `renv.lock` file unless you create a snapshot. 
Create a snapshot only when you are sure you want to include new packages to the list. Remember that the list of packages needs to be exactly what the project needs (minimum!). 

To create a snapshot do the following: 

```R
renv::snapshot() 
``` 

You can deactivate your environmnet at any moment (remember that this means you are outside of the project environment, so everything you install will be done on your local library!). 
 
```R
renv::deactivate()
```

The same if you want to activate the environment (this is done when you have already installed all needed packages and you just want to continue working): 

```R
renv::activate()
```


**renv folder** 

renv folder is automatically created by renv package the first time the renv environment is initialized. There you have the local library and important files to make it work. 
Do not touch them manually! 

