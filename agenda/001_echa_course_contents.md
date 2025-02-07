# The Role of Machine Learning in Chemical Risk Assessment; _Applications and Grounding Theory_

## **Michael Liem, PhD; Panagiotis (Panos) Karamertzanis, PhDMarc A.T. Teunis, PhD**

## 26 & 27 February, 2025

## Learning aims

After taking this course, participants have

 - A solid understanding of the principles of machine learning
 - Insight in applications of AI in the process of chemical risk assessment   
 - Have seen some hands-on examples on how to generate results from machine learning workflows
 
## 26 February, 2025 - Day 1 overview 

(9.30 - 17.00)

 1. 09:30 - 9:45 **General introduction** (15 min.) [all - Marc]
 1. 09:45 - 11:00 **Lecture 1**; Principles of machine learning (75 min.) [Marc]
 1. 11:00 - 11:15 ---- COFFEE ----
 1. 11:15 - 11:45 **Lab 0**; Getting to know Jupyter notebooks and Google Colab (30 min.) [Michael]
 1. 11:45 - 12:45 **Lab 1 - part 1**; General and Data preparation - get a feel for the data we have (60 min.) [Panos + Michael]
 1. 12:45 - 13:30 ---- LUNCH BREAK ---- (45 min.)
 1. 13:30 - 15:15 **Lab 1 - part 2**; Data conversion for Neural Network applications (60 min.) [Panos + Michael]
 1. 15:00 - 15:15 ---- TEA BREAK ---- (30 min.)
 2. 15:15 - 16:00; **Lab 1 - part 3**; Building the Feed Forward Neural Network (FFNN) (45 min.)
 1. 16:00 - 17:00 **Lecture 2** An introduction to foundation models (60 min.) [Marc]

## 27 February, 2025 - Day 2 Overview

(9.30 - 15.00)

 1. 09:30 - 10:30 **Lab 2 - part 1**; General preparation and train/test split (60 min.) [Panos + Michael]
 1. 10:30 - 10:45 ---- COFFEE ----
 1. 10:45 - 12:30 **Lab 2 - part 2**; Defining our model and evaluate prediction with K-fold cross validation (105 min.) [Panos + Michael] 
 1. 12:30 - 13:15 ---- LUNCH -----
 1. 13:15 - 14:15 **Lab 2 - part 3**; Learning curves and Hyperparameter tuning (60 min.) [Panos + Michael]
 1. 14:00 - 14:45 **Lecture 3**; Future of AI in chemical risk assessment (45 min.) [Marc]
 1. 14:45 - 15:00 Wrap-up

## Side Discussions 

14:00 - 16:00 Round Table Discussion - implementation of more advanced AI developments in chemical risk assessment 

## Detailed Course Contents

## Day 1 - Introduction

(30 min)

Introductions of the people, aim of the course, materials, getting started

## Day 1 - **Theory 1; Principles of Machine Learning**

(100 min)

Key Learning Concepts:

 - Principles of Machine Learning
 - What is AI, and which flavours? History of AI
 - Architecture - algorithm? Regression based vs neural network
 - What is a neural network, building blocks
 - Embedding; from data to numbers, examples, tensors, vectors
 - Features, feature space (materials from AIRA course)
 - Validation, cross-validation, leave-one-out, metrics of performance
 - Which models are used?

## Day 1 - **Lab 0; Introduction to Jupyter Notebooks**

(100 min) <- I would think this is a bit much for the introduction. Perhaps 30 min.
 
 - Running a notebook in Jupyter and running an ML model
 - First encouter: some exploratory data analysis and graphs
 - Simple matrix multiplication using CPUs and GPUs. Simple gradient calculations using CPUs and GPUs. Compare time of execution.
 - ...

## Day 1 - **Lab 1**; Introduction to Modelling 

(100 min)

### Data Loading and Exploration

Load the dataset: 
With structures and genotoxicity calls for Ames TA 98/100 with and without metabolic activation (four columns: positive, negative, equivocal). Acknowledge dataset preparation by ECHA, though preparation steps are not shown.
  
Explore the dataset: 

 - Number of substances per modelling task (with and without equivocal calls).
 - Distribution of genotoxicity calls.
 - Concordance of genotoxicity calls.
 - Visualisation of metabolic activation's importance.

Key Learning Concepts:

 - Binary, multiclass, and multilabel classification.
 - Issues in structure preparation and substance identity ambiguities.
 - Balanced vs. imbalanced datasets and balancing techniques.
 - Intuition and consistency checks for dataset validity.

### Descriptor Calculation

  - Use Morgan count and binary fingerprints, experimenting with length and radius.
  - Visualise example bits and molecules per toxprint.
  - Check for toxprint enrichment.

Key Learning Concepts
 
 - Different descriptors and fingerprints.
 - Assigning meaning to descriptors and their relation to endpoints.

### Model Fitting

  - Fit three models: Random Forest, XGBoost, and FFNN, using Morgan fingerprints.
  - Visualise performance metrics: balanced accuracy, F1 score, and AUC.
  - Demonstrate overfitting and the effect of random seed changes.

Key Learning Concepts

 - Classification models.
 - Prediction performance metrics.
 - Importance of feature engineering, especially for deep learning.

### Dataset Splitting

 - Train/test split and comparison of performance metrics.
 - Discussion of bias, variance, and overfitting detection.

## Day 1 - **Theory 2**; Concepts in Applied Modelling 

(100 min.)

This theroy is intermingled with Lab 1, and is meant as a foundation for the practical applications 
learned in Lab 1

Key Learning Concepts:

1. **Classification Concepts**:
   - Binary, multiclass, and multilabel classification.
   - Multitask modelling.

2. **Data Preparation and Validation**:
   - Importance of structure preparation.
   - Issues with substance identity ambiguities.
   - Balanced vs. imbalanced datasets and balancing techniques.
   - Checking dataset consistency with intuition.

3. **Descriptors and Fingerprints**:
   - Types of descriptors (e.g., Morgan fingerprints, toxprints).
   - Assigning meaning to descriptors and their relation to modelled endpoints.

4. **Model Training and Evaluation**:
   - Introduction to classification models: Random Forest, XGBoost, FFNN.
   - Metrics for prediction performance: balanced accuracy, F1 score, AUC.
   - Detecting overfitting and understanding bias/variance trade-offs.
   - Necessity and role of feature engineering in model performance.



Foundation models, do not forget xAI (explainable AI). post medium. 

## Day 1 - Closure / Evaluation 
 
(30 min.)

-----------------------------------------------------------------------------

## Day 2 - **Recap Day 1**

(30 min.)

## Day 2 - **Lab 2; A more realistic Application**

### Cross-Validation

 - Implement 5-fold cross-validation with FFNN architecture.
 - Limit epochs to 10 for efficiency, performing one fit per fold.

Key Learning Concepts

 - Necessity of cross-validation and nested cross-validation.
 - Data leakage.
 - Applicability domain and generalisation challenges.

### Hyperparameter Tuning

 - Conduct grid search on FFNN architecture with variations in layers and neurons (2x2 grid).
 - Select optimal model based on balanced accuracy.

Key Learning Concepts

 - Hyperparameter tuning challenges in deep learning.
 - Computation costs and trade-offs.

### Model Application

 - Use the optimal model to predict non-confidential REACH substances.
 - Vary probability cutoff for overall prediction statistics.
 - Identify and visualise predictions deviating from experimental results.

Key Learning Concepts

 - Using models for spurious data identification.
 - Iterative execution of modelling and data curation.

## Day 2 - **Theory 3; Assessing and optimizing model performance & model validation 

(100 min.)

This theroy is intermingled with Lab 2, and is meant as a foundation for the practical applications 
learned in Lab 2.

Key Learning Concepts:

1. **Cross-Validation**:
   - Importance of cross-validation and nested cross-validation.
   - Risks of data leakage.
   - Generalisation challenges and applicability domain.

2. **Model Generalisation**:
   - Low validation error does not guarantee good generalisation.
   - Training/validation sets may lack diverse chemistries needed for future predictions.

3. **Hyperparameter Tuning**:
   - Grid search for optimal model architecture.
   - Challenges of hyperparameter tuning in deep learning due to computational costs.

4. **Model Application and Iterative Improvement**:
   - Using models to identify spurious experimental data.
   - Modelling and data curation as iterative processes.

## Day 2 - **Theory 4**; Foundation Models & Their applications

(100 min.)

 - Generative AI & Foundation models 
 - Generative AI in toxicology
 - Ai for in vitro models (optimization of culture conditions), etc.
 - Agentic AI; emergence and applications - ToxPilot

## Day 2 - Closure / Evaluation  

(30 min.)

## General Remarks 

### **Prequisites for the Participants**

 - Access to Google Colab
 - Everybody needs to bring a laptop, with working WiFi connection
 - We need enough power-sockets to power all the laptops
 - A large screen in the room is handy, especially for the hands-ons
 - Enough coffee, tea and chocolate to power the brains ;-)
 - Find a good resource for the participants to use/go to after the course.



