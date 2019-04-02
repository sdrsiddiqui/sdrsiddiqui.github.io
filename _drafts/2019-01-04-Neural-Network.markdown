---
title:  Neural Networks
description: Data Science Basics
excerpt: Data Science Basics.

header:
    overlay_filter: "0.1"


tags:
  - Data Science

---


Networks of non-linear elements, interconnected through adjustable weights,play a prominent role in machine learning. They are called neural networks because the non-linear elements have as their inputs a weighted sum of the outputs of other elements—much like networks of biological neurons do. These networks commonly use the threshold element which we encountered in chapter two in our study of linearly separable Boolean functions. We begin our treatment of neural nets by studying this threshold element and how it can be used in the simplest of all networks, namely ones composed of a single threshold element.


At the heart of neural networks is the unit (also called a node or neuron). A unit takes in one or more inputs, multiplies each input by a parameter (also called a weight), sums the weighted input’s values along with some bias value (typically 1), and then feeds the value into an activation function. This output is then sent forward to the other neurals deeper in the neural network (if they exist). Feedforward neural networks—also called multilayer perceptron—are the simplest artificial neural network used in any real-world setting.

Neural networks can be visualized as a series of connected layers that form a network connecting an observation’s feature values at one end, and the target value (e.g., observation’s class) at the other end. The name feedforward comes from the fact that an observation’s feature values are fed “forward” through the network, with each layer successively transforming the feature values with the goal that the output at the end is the same as the target’s value.



An artificial neural network is a model of computation inspired by the structure of neural networks in the brain. In simplified models of the brain, it consists of a large number of basic computing devices (neurons) that are connected to each other in a complex communication network, through which the brain is able to carry out highly complex computations.
Artificial neural networks are formal computation constructs that are modeled after this computation paradigm. Learning with neural networks was proposed in the mid-20th century. It yields an effective learning paradigm and has recently been shown to achieve cutting edge performance on several learning tasks.

A neural network can be described as a directed graph whose nodes correspond to neurons and edges correspond to links between them. Each neuron receives as input a weighted sum of the outputs of the neurons connected to its incoming edges. We focus on feedforward networks in which the underlying graph does not contain cycles.
