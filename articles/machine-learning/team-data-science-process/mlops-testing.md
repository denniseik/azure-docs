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
# Testing AI Solutions

A tested code base is an important factor contributing to the production-readiness of an AI application. Other than the code base of a traditional software application, the quality of the build of an AI application is for a much larger factor influenced by the combination of code and data. Hence, both code testing and data testing are essential to ensure the proper functioning of our application under different data conditions. We can discover problems at an early stage through continuous feedback and testing is one great feedback tool we use in software engineering. There are various test types applicable for an AI application.

* _Unit tests_ - Individual components of the codebase are tested separately. In a data science project imaging each transformation on the data set has its own unit test. 
* _Data tests_ - Tests to validate that the input schema complies with the data dictionary that was created during the data acquisition and data understanding phase. 
* _Model validation tests_ - Ensures that the responses of the model are in an expected range. For example if the model is returning probabilities, you should ensure that the output is between 0 and 1 as 1.2 would not make any sense.
* _Integration tests_ - All individual software modules are combined and tested as a group. In the data science context this includes the ingestion process, the scoring modules and perhaps even the integration with the overall digital experience we are aiming for.
* _Data skew tests_ - Tests that the distributions of each feature in the incoming data set as similar to what was documented in the data acquisition and understanding phase. If the distribution changes over time, then perhaps this is an indication that the model may need to retrain.
* _Load tests_ - Ensures that the model can respond in parallel to multiple requests and within time. Usually load testing is used to do capacity planning and scale up/out the solution to meet the customer's target non functional requirements (e.g. response within 500ms for 300 concurrent users).
