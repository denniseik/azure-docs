---
title: MLOps (DevOps practices)
description: An overview of devops practices for AI solutions
services: machine-learning
author: denniseik
manager: cgronlun
editor: cgronlun
ms.service: machine-learning
ms.subservice: team-data-science-process
ms.topic: article
ms.date: 14/06/2019
ms.author: tdsp
ms.custom: seodec18
---
# Managing Infrastructure and Configurations as Code

## Infrastructure-as-Code
“_Infrastructure as Code (IaC)_ entails defining environments, including networks, servers, and other compute resources, as a text file (script or definition) that is checked into version control and used as the base source for creating or updating those environments. For instance, adding a new server should be done by editing a text file and running the release pipeline, not by doing a remote connection into the environment and spinning up one manually.” - MPP DevOps

Applying infrastructure-as-code will bring you the benefits of environment consistency, more speed in deployment, and lower risks (e.g. less chance for environment-specific errors / security violations). As a data team, IaC could help you to describe/deploy/manage your training or operationalization environment(s) in a consistent way.

## Configuration-as-Code
'_Configuration-as-Code_' helps you to describe the configuration of your infrastructure as code. As a data scientist this could help you to generate a similar working environment on another machine that has, for example, all the packages available that your code needs in order for it to run.

As you start a new project, you’ll likely install the latest version of Python and the latest version of packages. Your code will run fine on your computer, but what if you need to share your code with a colleague? If he or she runs another version of python or has different or other versions of packages installed, your code may either not run successfully or may behave differently than intended. For example, a model that you train with one version of the scikit-learn package, might give other predictions when running a different package version. Another scenario might be that you want to run your model training on another type of infrastructure, a DSVM for example or Azure ML Compute. You want then to be sure that your code is run with the same dependencies as those that you expect.

These are just two examples of why we want to aim for a reproducible environment. A first action we can take to achieve this goal is to actually start tracking which python packages (and their versions) our project requires. Natively in python, you could use requirements.txt file for this. Conda is a package manager that can help us in addition to create _isolated environments_. This will allow us to create different python environment on our computer, for example one for project A that requires python 2.7, and one for project B that requires python 3.3 with pandas 0.23. You will have to keep track of the packages you install in order to be able to share a clean environment with your colleagues.

## Further Learning
* [What is Infrastructure-as-Code?](https://docs.microsoft.com/en-us/azure/devops/learn/what-is-infrastructure-as-code)