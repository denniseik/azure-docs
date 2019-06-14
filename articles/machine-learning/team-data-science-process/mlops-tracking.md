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
# Experiment Tracking

Model training is an iterative process. When experimenting, you may combine different features, hyperparameters, data samples, may try different ways of aggregation, and hence you have to keep track of what specific experiment set up led to what model performance to allow for comparison.

This does help you in three main ways: *1) it supports your model selection process 2) it helps steer your experimental process/direction 3) it allows for reproducability*.

Say you are in an early phase of your data science project, and you find yourself in a situation where you have the impression that the model you came up with a few hours ago, or rather a week ago was actually performing better that what you have now... can you then reproduce that partical experiment?

Reproducability for models, and later AI Solutions, would require you to keep track of what *code* and what *data* was used to lead to a certain *outcome* e.g. a model. Hence, creating a code and data snapshot with each run of your experiment is an important practice. Beyond just code and data, additional tracking of the environment configuration (e.g. package versions) would enable you to reproduce similar results. In pipeline scenarios, where you may be passing in- and output datasets to different steps, this would also mean to version those artifacts.
