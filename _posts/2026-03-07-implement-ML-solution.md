---
layout: post
title: "Implementing Machine Learning Solutions"
date: 2026-03-07 09:45:00 -0800
categories:
   - machinelearning
---

The Software Development Lifecycle (SDLC) is the process employed by software engineers to balance high quality software solutions with short time implementation. Agile methodologies are often used for this process. Machine learning (ML) also follows a lifecycle, called the Machine Learning Lifecycle (MLL), with distinct stages.

The conventional SDLC stages are:  
  1. Problem formation and understanding
  2. Data collection and preparation
  3. Model training and testing
  4. Model deployment and maintenance  

Problem formation and understanding entails exploring current business processes to discern where ML has useful implementation. Not every problem can or should be solved with ML. It is important to ask if ML is an ethical solution to the proble, potential inputs/outputs, and predicted error rates for positive and false negatives. What do you need from an accuracy perspective?

Data collection and preparation is where one sources the data they need for their projects. It may come from an internal repository, a client provides data, open-source data from public repositories, or data purchased from a third party. This "raw data" is not in an accessible state for a machine. Most time in the MLL is dedicated to annotating, wrangling, labeling, removing irrelevant features, outliers, and transforming the missing values so it is usable for a computer.

For model training, 80% of the data is typically reserved. 10% is used for validation using known good data, and 10% is used for testing with new data. This split is significant because it helps to validate the model for data it was not trained on. The appropriate ML algorithm is selected to start the training process. Multiple passes are made to produce the model. This model is iterated and fine-tuned over time before the model is put in to the production stage.

During model deployment and maintenance, a "cadence" is set up for retraining and monitoring overall performance. The MLL is significant because it is an iterative process that continually feeds back into itself to ensure a well-performing model responds to changes in the data and needs in consumer demands.

It is key to frame the ML problem in proper context. People find ML a hot topic, but it is not the solution to all problems, and can cause more problems. If one can use simpler rules, computations, or pre-determined steps to solve a problem, ML is not necessary. ML works best with predicting an outcome, uncovering trends, implementing rules that cannot be coded, or large data that people cannot process.

If ML is a good fit, framing the problem helps determine the goals and success criteria early on. We frame the problem by defining what questions the model will answer and what the necessary inputs and outputs are. This will help with proper algorithm selection. If answering a yes/no question, it is key to use a binary classfication algorithm like AWS Linear Learner. If answering a numeric/continuous value output, it is better to use the XGBoost algorithm. At the start, we can think about the relationships between the features and how each feature will predict the target. For example, visual features in an imaging photo to predict the likelihood of early tumor development or aspects of the real estate market that predict the value of a house on the market.

The next consideration is how model output integrates into existing applications. The prediction should be turned into action to help clients or stakeholders. For example, it may be possible to use an ML algorithm to match new clients with products they would like at a supermarket by training off previous customer data. A success metric would be improved sales across the supermarket. It is also key to appropriately budget for long-term costs and maintenance to make sure computing costs do not exceed the value provided by the ML model.

When starting an ML project, two options are to train your own model or to use an existing pre-built model. Obtaining enough data to get good performance is difficult for individuals or smaller organizations, so using a larger model can be more helpful to save time and money. Image classification models usually use pre-existing models via "transfer learning", which allows one to add new data on top and inheret the new learning from the added data. This is significant because one can use previous known-good methods for reusability and efficiency. The disadvantage is that if the necessary data is not included, such as a facial recognition algorithm biased towards specific groups, it makes it more difficult to add new data on top reliably.

One may find pre-trained models through ModelZoo, which curates pre-existing deep learning models on computer vision, natural language processing, audio, speech, video, and others. Most models are released under the Apache 2.0 license, indicating software developers can modify the code freely, copy the original course code, and modify/distribute the source code. The AWS MarketPlace also provides pre-trained ML models.and deployed on Amazon SageMaker, a cloud-based ML platform. Some are free and others require one-time purchase. Hugging Face provides pre-trained models for natural language processing for sentiment analysis, questions and answers, translations, and summarizing texts.

If pre-trained models do not solve the problem, the solution is to train a custom model. With a large enough data set and sufficient processing power, one can run an ML model. ML models usually require computationally invensive processing power and hardware to support it. Simple models can train on a laptop central processing unit (CPU). For more complex models, GPUs are required for training and cannot be done on a laptop. Cloud resources such as AWS or Google Cloud are necessary. Hardware needs are dictated by the problem to solve, chosen learning algorithm, and selected ML framework.

It is possible to train custom models in many languages including R, Python, and Java. Python is the most popular language since it is an easier language to learn that can be used outside of the ML context and has great libraries. The following blog posts will use Python.

The Integrated Development Environment (IDE) for ML in Python is a Jupyter Notebook. These notebooks provide a platform for data analysis, visualization, and training code. Python-based data analytic tools include Numpy and Pandas libraries. Pandas is for solid state data structures, N-dimensional matrices, and exploratory data analysis for CSV, JSON, and TSV data files. Numpy is for numerical computing for multidimensional array or matrix support. Matplotlib and Seaborn are Python-based 2D plotting libraries for creating visualizations to corroborate your ML analysis. ML framework libraries include Scikit-learn, TensorFlow, MXNext, PyTorch, Keras, and others.

From the basic introduction of Python libraries, one may use them for the ML process. 
