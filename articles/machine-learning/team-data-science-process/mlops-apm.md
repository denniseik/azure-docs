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
# Application Performance Monitoring

Understanding how your application is performing once deployed is an important mean to learn from your users, understand the load on your application, hence if you need to scale or optimize, or to resolve issues that may be occuring with your end users.

This isn't only relevant for traditional software applications, this is even more relevant as soon as you have deployed your model on a serving app - practically in many cases, as soon you have deployed your model it can be considered already old. New data may be different from the data that you trained your model with, hence the environment will drift. Monitoring will help you to discover this and take action.

On a high-level we can distinguish different types of monitoring to think about:

* Monitoring for Concept drift
  * Monitor Data / Model Quality
  * Establish data feedback loop.
  * Trigger retraining flow on set KPIs.

* Monitoring the Model Serving Application
  * Monitor request load and activities on real-time model scoring webservices.

* Logging for reproducability / operability
  * Log new model in- and outputs, model version
  * Version dataset and codebase that led to model artifact.
  * Version and log data pipeline execution that led to model input
