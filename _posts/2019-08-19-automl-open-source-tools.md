---
layout: post
title:  "Open source AutoML & Optimization tools"
date:   2019-08-19 16:16:01 -0600
categories: Python, AutoML, Machine Learning
seo:
    type: BlogPosting
    name: "Open source AutoML and Optimization tools"
---


# What's that?

I was looking for an open-source alternative that mimic AutoML's algorithm.
This can be implemented in various ways such as brute force, genetic algorithms and more.
I've created a list of libraries/frameworks to help you choose one. 


### To the list!

[EpistasisLab/tpot: A Python Automated Machine Learning tool that optimizes machine learning pipelines using genetic programming.](https://www.notion.so/ac33ca8bf76d4cd382173857885bdd12)

[](https://www.notion.so/ac33ca8bf76d4cd382173857885bdd12#d46434ca57fd4175ba741f9fe27fec56)

Consider TPOT your **Data Science Assistant**. TPOT is a Python Automated Machine Learning tool that optimizes machine learning pipelines using genetic programming.

TPOT Demo (credit - TPOT website)

[](https://www.notion.so/ac33ca8bf76d4cd382173857885bdd12#66f19a9f1fc541c1a19329d73832694d)

TPOT will automate the most tedious part of machine learning by intelligently exploring thousands of possible pipelines to find the best one for your data.


[AutoML: Automatic Machine Learning — H2O 3.26.0.2 documentation](https://www.notion.so/3da787cae15c4a1a869ab38b49d0a2a5)

H2O’s AutoML can be used for automating the machine learning workflow, which includes automatic training and tuning of many models within a user-specified time-limit. Stacked Ensembles – one based on all previously trained models, another one on the best model of each family – will be automatically trained on collections of individual models to produce highly predictive ensemble models which, in most cases, will be the top performing models in the AutoML Leaderboard.

[Ax · Adaptive Experimentation Platform](https://github.com/facebook/Ax)
**Adaptive Experimentation Platform**
![AX Logo](https://github.com/facebook/Ax/raw/master/website/static/img/ax_logo_lockup.svg)

Developers and researchers alike face problems where they are confronted with a large space of possible ways to configure something –– whether those are "magic numbers" used for infrastructure or compiler flags, learning rates or other hyperparameters in machine learning, or images and calls-to-action used in marketing promotions. Selecting and tuning these configurations can often take time, resources, and quality of user experiences. Ax is a machine learning system to help automate this process, and help researchers and developers get the most out of their software in an optimally efficient way.

Ax is a platform for optimizing any kind of experiment, including machine learning experiments, A/B tests, and simulations. Ax can optimize discrete configurations (e.g., variants of an A/B test) using multi-armed bandit optimization, and continuous (e.g., integer or floating point)-valued configurations using Bayesian optimization. This makes it suitable for a wide range of applications.

Features:
- Hyperparameter Optimization for PyTorch
- Multi-Task Modeling
- Benchmarking Suite
- Bandit Optimization
- Human-in-the-Loop Optimization
- Visualizations

[pytorch/botorch: Bayesian optimization in PyTorch](https://www.notion.so/064dc36cf0ad4b1f860037b7a1cb6e25)
**Botorch Beta**
[](https://www.notion.so/8edbb98b116e446fb6cf5284cc947813#e9645aa9267f4a2abdedf79f44d68c3f)

BoTorch is a library for Bayesian Optimization built on PyTorch.

Provides a modular and easily extensible interface for composing Bayesian optimization primitives, including probabilistic models, acquisition functions, and optimizers.


[auto-sklearn — AutoSklearn 0.5.2 documentation](https://www.notion.so/c7950c4bf07e4150bb37e9c0eb07b27f)
**auto-sklearn is an automated machine learning toolkit and a drop-in replacement for a scikit-learn estimator**
auto-sklearn frees a machine learning user from algorithm selection and hyperparameter tuning. It leverages recent advantages in Bayesian optimization, meta-learning and ensemble construction. 


[ypeleg/HungaBunga: HungaBunga: Brute-Force all sklearn models with all parameters using .fit .predict!](https://github.com/ypeleg/HungaBunga)

**Hunga-Bunga**

Brute Force all scikit-learn models and all scikit-learn parameters with **fit** **predict**.

### Lets brute force all sklearn models with all of sklearn parameters! Ahhh Hunga Bunga!!

    from hunga_bunga import HungaBungaClassifier, HungaBungaRegressor

### And then simply:

[](https://github.com/ypeleg/HungaBunga/raw/master/HungaBunga.png?raw=true)

*****
