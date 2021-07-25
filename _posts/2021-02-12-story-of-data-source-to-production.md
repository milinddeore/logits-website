---
layout: single
title: "Story Of Data — Source To Production"
categories:
  - Data
tags:
  - Data
---
<figure class="center">
  <img src="/assets/images/StoryOfData.png" alt="">
</figure>

Business analysts understand the business needs and pass the requirements to the data analyst.

Data analysts understand the data requirements and determine what data is needed to address a business problem. Data analyst then collects the right data from an internal source, or by curating the data (*eg.: scraping*), or from an external source (*eg.: open datasets, Kaggle, research projects*). The raw data needs to get processed before the machine learning team can use it. This is a critical step and hence **‘become one with data’**.

Usually the data is divided into two categories (at high level):

**1. Structured Data** : CSV, Tabular form data, Columnar, etc.

**2. Unstructured Data** : Images, audio, video, text, etc.

Based on business needs, data analysts collect appropriate training, validation, and test datasets. The data MUST be similar to the real world data, else there will be high variance in the results. Rachel Thoma’s blog [How (and why) to create a good validation set](https://www.fast.ai/2017/11/13/validation-sets/), describes it neatly.

The data comes from multiple sources and we need to collect it through data pipelines and possibly aggregate it into a database / data-lake.

**1. Data Engineering** :
- Collection / Storage,
- Ingestion,
- Preparation / Transformation (*Clean, Shape, Augment, Transform, Feature Extraction, Conform*).

**2. Machine Learning** : Computation

**3. Output** : Inference, Presentation

Spending time in understanding the data distribution and finding the outliers is pivotal, the human brain is excellent at this job, hence data analysts must inspect the data manually first. Primarily, during cleaning we are trying to find missing labels, incorrect labels, duplicates, incomplete data, missing fields, etc.

With my personal experience, data dimensionality reduction is a very important step, it not just gives better data insight but also reduces the model size, that means low compute power, low memory requirement, fast training time and much better results. It’s an analyst’s job to find how much details actually matter and thereby how many features need to be captured.

The model must be initialised with proper random seed, and data must be normalised and standardised for training, the same normalisation and standardised parameters must be used during inference also. Data augmentation is cosmetic change on images, and at times gives better results, it shouldn’t be too overwhelming.

A data designer is usually worried about how the data is stored, meaning he/she tries to understand the relationships between the incoming data field and design the structure so that it can be stored. This data has to be managed properly with security access such that only authorised people should have access to it, and has to be backed up too. This is the time when data administrators must consider [GDPR and CCPA compliance](https://mdeore.medium.com/dataset-assessment-framework-2ab1499d054a), meaning removing customer’s personal information linkage and assigning Artificial ID, this process is called Pseudonymization.

Machine learning researchers create various machine / deep learning models or explore variations of existing models that can be used for business purposes. Data scientists experiment with such models and play around with model parameters to find the best fit. These are called hyper parameters: Optimiser, Regularisation, Drop-outs, Batch-size, Learning-rate are some important hyper-parameters that need to be tuned to converge model to best fit on a particular dataset. Andrej Karpathy’s blog gives more insights [‘A Recipe for Training Neural Networks’](http://karpathy.github.io/2019/04/25/recipe/).

During training, a series of evaluation metrics are monitored, to reduce the loss and let the model to converge. This is an iterative process until data best fit with lowest possible loss. Once the model converges, it is then verified with a test-set, ideally with real world dataset, this is called inference.

For deployment, models can be transformed from one framework to another using ONNX. For mobile deployment, it can be converted to `.tflite` format, which utilises flat-buffers instead of protocol-buffers, for fast load-time on mobiles. At this stage we can also perform quantisation on the frozen model from `float` to `int8`. Quantisation techniques reduce the model size at the cost of slight degradation in accuracy, this is again based on the business needs, how much quantisation is required Vs accuracy compromise.

![Data Processing Pipeline](/assets/images/DataProcessDeployment.png)

Finally, end-to-end business processes and technology is employed to deploy the model that enables the business to ultimately serve its customers.
