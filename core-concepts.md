# Data

* Machine learning systems learn from examples, not rules.

* Data is a collection of input–output pairs

* The input is what the model sees

* The output is what we want the model to predict

## Example:

* Input: an image of a handwritten digit

* Output: the correct digit (0–9)

The quality of a model is heavily dependent on the quality and diversity of data.

# Features

A feature is a measurable property extracted from data.

In images: pixel intensity values

In audio: amplitude, frequency components

In signals: samples, coefficients, energy values

Neural networks learn useful features automatically across layers.

# Model

A model is a mathematical function that maps inputs to outputs.

In a neural network:

the model consists of neurons

weights and biases define its behavior

Changing weights changes the model.

# Parameters

Parameters are the internal numbers the model learns.

For neural networks, parameters are:

* weights

* biases

Learning is the process of adjusting these parameters to reduce errors.

# Training

Training is how a model learns.

It involves:

* Making a prediction

* Comparing it with the correct answer

* Measuring the error

* Adjusting parameters to reduce that error

This process is repeated over many examples.

# Loss Function

A loss function measures how wrong a prediction is.

* Small loss → good prediction

* Large loss → poor prediction

The goal of training is to minimize loss.

Example:

Predicted digit = 3

Actual digit = 5

Loss quantifies how bad this mistake is

# Optimization

Optimization is the process of reducing loss.

Most models use gradient descent, which means:

change parameters slightly

move in the direction that reduces loss

Over time, the model improves.

# Generalization

A good model should:

perform well on data it has seen

perform well on new, unseen data

This ability is called generalization.

Models that memorize training data but fail on new data are said to overfit.

# Overfitting vs Underfitting

* Overfitting: model is too complex, memorizes data

* Underfitting: model is too simple, misses patterns

Good models balance complexity and simplicity.

# Inference

Inference is using a trained model to make predictions.

Training happens once (or occasionally)

Inference happens every time the model is used

In hardware systems, inference is usually the main focus.

## Supervised Learning

* In supervised learning:

* each input has a correct label

* the model learns by comparing predictions with labels

Most neural network examples fall into this category.

## Unsupervised Learning

In unsupervised learning:

* no labels are provided

* the model finds patterns on its own

Examples include clustering and dimensionality reduction.

# Why this matters for hardware systems

In hardware-accelerated ML:

* training is often done offline (CPU/GPU)

* inference is deployed on FPGA or embedded systems

This makes:

* efficiency

* latency

* power consumption

* critical design considerations.

Final Summary

* ML systems learn from data, not rules

* Models are defined by parameters

* Training adjusts parameters to minimize loss

* Good models generalize to new data

* Inference is the deployed, real-time phase
